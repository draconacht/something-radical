---
title: boolean algebra simplifies conditionals
categories:
  - general programming
date: 2024-08-03T18:30:00.000Z
---

this should go without saying, but knowing and applying boolean algebra laws can simplify a lot of code. this is especially useful when tasked with rewriting legacy code, a lot of which may be unoptimised and filled with deprecated features.

here are some tools that will help you with this task:

* De Morgan's laws
* early returns, especially when combined with negation
* 0 & X = X, 1 & X = X, 0 | X = X, 0 & X = 0

here's an example

```python
for student in students:
  if student.marks > 35:  # passed course
    if student in honor_students_for_course:
      if student.marks > 80:
        student.grade="A+"
      else:
        student.grade="A"
    elif 60 < student.marks and student.marks <= 70:
      student.grade="B"
    elif 50 < student.marks and student.marks <= 60:
      student.grade="C"
  else:
    student.grade="F"
    student.fail=True

```

at first sight, this code might not look so bad. i'm sure almost everyone has written code for a class assignment at some point that looks like this. but sit with it for a minute and think how it might be improved.

```python
for student in students:
  if student.marks > 35:  # this is really far from
    if student in honor_students_for_course:
      if student.marks > 80:
        student.grade="A+"
      else:
        student.grade="A"
    elif 70 < student.marks and student.marks <= 80:
      student.grade="B"
    elif 60 < student.marks and student.marks <= 70:
      student.grade="C"
  else:                  # this!
    student.grade="F"
    student.fail=True
```

a conditional with a large success and small failure case is a sign that you can use an early return pattern here. this is often the case with validation conditionals.

```python
for student in students:
  if student.marks <= 35:
    student.fail=True
    student.grade="F"
    continue
  if student in honor_students_for_course:  # everything here is now one indent shallower
    if student.marks > 80:
      student.grade="A+"
    else:
      student.grade="A"
  elif 70 < student.marks and student.marks <= 80:
    student.grade="B"
  elif 60 < student.marks and student.marks <= 70:
    student.grade="C"
```

while the lines of code might have not changed, the logic is clearer to read now. additionally, you have performed the same task while needing less indentation. this is great because if you've ever seen bad code (enterprise, research, or academic), you know how deep they run. not only does it occupy more space, if you use word wrap (like i do) you have to move your eye down to read the next line, which makes it that much more frustrating to parse.

else cases are rarely necessary. very often, you can remove them by putting the default handling at the top. this isn't necessarily going to make your code cleaner, but it does make the logic shorter.

additionally nested if cases can often be swapped between layers. this may or may not make your logic cleaner.

```python
for student in students:
  if student.marks <= 35:
    student.fail=True
    student.grade="F"
    continue
  if student.marks > 80:  # looser condition comes first
    student.grade="A"
    if student in honor_students_for_course  # tighter condition comes second
      student.grade="A+"
  elif 70 < student.marks and student.marks <= 80:
    student.grade="B"
  elif 60 < student.marks and student.marks <= 70:
    student.grade="C"
```

lastly, watch out for logical repetitions. if you've reached an else statement, everything in an if statement before it is untrue. keeping this in mind can help you spot redundant checks and remove them

```python
for student in students:
  if student.marks <= 35:
    student.fail=True
    student.grade="F"
    continue
  if student.marks > 80:  
    student.grade="A"
    if student in honor_students_for_course  
      student.grade="A+"
  elif student.marks > 70:  # getting here means the student definitely scored too less for an A
    student.grade="B"
  elif student.marks > 60:  # getting here means the student definitely scored too less for a B
    student.grade="C"
```

sometimes, rearranging if-elseif chains can also help you spot and remove redundant conditions.

happy refactoring.
