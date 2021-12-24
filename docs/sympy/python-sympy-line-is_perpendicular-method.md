# Python | Sympy line . is _ vertical 方法

> 原文:[https://www . geesforgeks . org/python-sympy-line-is _ vertical-method/](https://www.geeksforgeeks.org/python-sympy-line-is_perpendicular-method/)

In Sympy, the function `is_perpendicular()` is used to check whether the two linear entities are perpendicular or not.

```
Syntax: Line.is_perpendicular(l2)

Parameters:
 l1: LinearEntity
 l2: LinearEntity

Returns:
 True: if l1 and l2 are perpendicular,
 False: otherwise.
```

**示例#1:**

```
# import sympy and Point, Line
from sympy import Point, Line

p1, p2, p3 = Point(0, 0), Point(1, 1), Point(-1, 1)

l1, l2 = Line(p1, p2), Line(p1, p3)

# using is_perpendicular() method
isPerpendicular = l1.is_perpendicular(l2)

print(isPerpendicular)
```

**输出:**

```
True
```

**示例#2:**

```
# import sympy and Point, Line
from sympy import Point, Line

p1, p2, p3 = Point(0, 0), Point(1, 1), Point(5, 3)

l1, l2 = Line(p1, p2), Line(p1, p3)

# using is_perpendicular() method
isPerpendicular = l1.is_perpendicular(l2)

print(isPerpendicular)
```

**输出:**

```
False
```