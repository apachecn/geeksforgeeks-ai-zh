# Python | Sympy line . is _ parallel()方法

> 原文:[https://www . geesforgeks . org/python-sympy-line-is _ parallel-method/](https://www.geeksforgeeks.org/python-sympy-line-is_parallel-method/)

In Sympy, the function `is_parallel()` is used to check whether the two linear entities are parallel or not.

```
Syntax: Line.is_parallel(l2)

Parameters:
 l1: LinearEntity
 l2: LinearEntity

Returns:
 True: if l1 and l2 are parallel,
 False: otherwise.
```

**示例#1:**

```
# import sympy and Point, Line
from sympy import Point, Line

p1, p2 = Point(0, 0), Point(1, 1)
p3, p4 = Point(3, 4), Point(6, 7)

l1, l2 = Line(p1, p2), Line(p3, p4)

# using is_parallel() method
isParallel = Line.is_parallel(l1, l2)

print(isParallel)
```

**输出:**

```
True
```

**示例#2:**

```
# import sympy and Point, Line
from sympy import Point, Line

p1, p2 = Point(0, 0), Point(1, 1)
p3, p4 = Point(3, 4), Point(6, 6)

l1, l2 = Line(p1, p2), Line(p3, p4)

# using is_parallel() method
isParallel = Line.is_parallel(l1, l2)

print(isParallel)
```

**输出:**

```
False
```