---
title: serialising typed data in python
categories:
  - python
date: 2024-11-09T18:30:00.000Z
---

## problem statement

serialising and deserialising objects is a pretty important part of operating with data. thankfully `json.dumps()` and `json.loads()` do most of the job for you. those functions are fine when you're operating with untyped data (everything being in dicts, lists, etc.), but dataclasses are often much better for organising your python data. they make your typing hierarchy more explicit, and enable you to use OOP concepts like polymorphism and inheritance.

say you start with these dataclasses

```python
@dataclass
class Slow(Ability):
  chance: int = 0
  duration: int = 0

@dataclass
class Freeze(Ability):
  chance: int = 0
  duration: int = 0

...

@dataclass
class Unit:
  hp: int = 0
  atk: int = 0
  abilities: list[Ability] = None
```

now let's try to serialise an object.

```python
unit = Unit(
    hp=100,
    atk=100,
    abilities=[Slow(100, 30), Freeze(100, 30)]
)
json.dumps(dataclasses.asdict(unit), indent=2)
```

```json
{
  "hp": 100,
  "atk": 100,
  "abilities": [
    {
      "chance": 100,
      "duration": 30
    },
    {
      "chance": 100,
      "duration": 30
    }
  ]
}
```

this isn't nice. 

### analysing the problem

let's think for a moment what the problem exactly is. 

* data that should have been human-readable is no longer human-readable. 
* data has been mutated in a way that cannot be reversed. polymorphic information has been lost, making deserialisation impossible.

### why not pickles?

seems like pickling is a viable solution here! it's surely the most effortless way to preserve typed data that can be conveniently deserialised. but it doesn't fix the first problem. in my particular case, i want my data to be human readable, so i can pass it through diffs or what not. that, and i don't like pickles in general.

## solutions

### adding a string field to the dataclass

```py
@dataclass
class Ability:
  _klass: str = ""

@dataclass
class Slow(Ability):
  _klass: str = "slow"

  chance: int = 0
  duration: int = 0

@dataclass
class Freeze(Ability):
  _klass: str = "freeze"

  chance: int = 0
  duration: int = 0

@dataclass
class Unit:
  hp: int = 0
  atk: int = 0
  abilities: list[Ability] = None
```

let's not think about deserialising for now. adding the class name attribute would fix the information problem, right?

> it's common to call `class` as `klass` in variable names to avoid overlapping with the keyword. i add a leading underscore to denote that the variable is private and should not be touched.

```json
{
  "hp": 100,
  "atk": 100,
  "abilities": [
    {
      "_klass": 100,
      "chance": 30,
      "duration": 0
    },
    {
      "_klass": 100,
      "chance": 30,
      "duration": 0
    }
  ]
}
```

right. adding an attribute also puts it in the constructor parameters. this isn't what i wanted. of course i could put `_klass` at the end of the class, but that doesn't make sense! i don't want the attribute in my constructor.

#### class variables

```py
from typing import ClassVar

@dataclass
class Ability:
  _klass: ClassVar[str] = ""
```

this is a nice and pythonic solution. dataclasses can handle [class variables](https://docs.python.org/3.12/library/dataclasses.html#class-variables) specifically. this sounds good because `_klass` is in fact a class variable, skipping it from constructors. but unfortunately class variables are skipped during dataclass serialisation, so that doesn't work for us.

### defining fields explicitly

dataclasses provide a more granular interface for modifying field behaviour. 

```py
@dataclass
class Ability:
  _klass: str = dataclasses.field(init=False, default="")
```

this provides the behaviour that i need.

> the [field](https://docs.python.org/3.12/library/dataclasses.html#dataclasses.field) function also describes other useful behaviours, like `default_factory` and `hash` functions for the field.

```json
{
  "hp": 100,
  "atk": 100,
  "abilities": [
    {
      "_klass": "slow",
      "chance": 100,
      "duration": 30
    },
    {
      "_klass": "freeze",
      "chance": 100,
      "duration": 30
    }
  ]
}
```

## deserialisation

### object_hook

[json.load()](https://docs.python.org/3.12/library/json.html#json.load) has a flag that allows you to control deserialisation behaviour.

```py
def object_hook_ability(dct: dict[str, any]):
    if '_klass' in dct:
        name = dct.pop("_klass")
        return model_lookup[name](**dct)
    return dct

...

e = json.load(fl, object_hook=object_hook_ability)
```

first, we check if the attribute `_klass` is present in the dict being deserialised, then cast it into an object if it is. finding the object class by the class name will require building a lookup dict, which i'll explain next.

also, dictionary unpacking helps! dataclasses give us a constructor with named parameters, so we can pass the values through dict unpacking. for objects that don't follow our `_klass` pattern, we will just return the dict as is.

### building the lookup table

the naive solution is to make a dictionary ourselves,

```py
model_lookup = {"slow": Slow, "freeze": Freeze}
```

this is nice, and might be enough for your use case. but i have a _lot_ of model classes, and don't really want to keep track of all of them.

```py
model_lookup={}
subclasses = []
subclasses_next = [Model]

while subclasses_next:
  temp = []
  for _klass in subclasses_next:
    temp.extend(_klass.__subclasses__())
  subclasses.extend(subclasses_next)
  subclasses_next=temp

for model in subclasses:
  if dataclasses.is_dataclass(model):
    try:
      a = model()
      model_lookup[a._klass] = model
    except AttributeError:
      pass
```

the above solution performs breadth-first-traversal on all the subclasses of a base `Model` class. for each dataclass inherited from `Model`, i instantiate an object and pass its `_klass` into my lookup dict.

as a side effect, i need to import all of Model's children, to setup the value of `__subclassess__()` correctly. this is a bit hacky, but overall something i can live with.

## other approaches

at this level of hacky-ness, it's best to consider a library that abstracts these details away. i was recommended to use [PyDantic](https://docs.pydantic.dev/latest/), which may or may not work better for your usage. 

also, this solution tries to circle the square of `dataclasses.asdict()`. it's not necessary to serialise dataclass objects through that route, and it might fall short for your usage. i can imagine making your own serialisation function / encoder that also serialises the class name implicitly.