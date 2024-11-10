---
title: genexp ouroboros
categories:
  - python
date: 2024-08-03T18:30:00.000Z
---

here's a code that generates [power sets](https://www.wikiwand.com/en/Power_set) over a list.

```python
out = [[]]
for num in num_list:
  out.extend(x+[num] for x in out)
```

it's lovely. it's concise. it's pythonic. it's mathematically elegant. it also contains an infinite loop!

the code inside the extend function evaluates to a generator expression, which is lazily loaded. modifying what you iterate over is never a good idea!

but this outcome is non-trivial. one would imagine that extend extends a chunk to an existing list. but with generator expressions, this chunk is loaded lazily. as extend pumps elements to the tail of the list, the generator sees a broader horizon to iterate over, and the loop goes on forever.
