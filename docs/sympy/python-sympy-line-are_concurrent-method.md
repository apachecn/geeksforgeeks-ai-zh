# Python | Sympy line . are _ concurrent 方法

> 原文:[https://www . geesforgeks . org/python-sympy-line-are _ concurrent-method/](https://www.geeksforgeeks.org/python-sympy-line-are_concurrent-method/)

In Sympy, the function are_concurrent() is used to check whether the given linearentities(lines) are concurrent or not. Two or more linear entities are concurrent ifthey all intersect at a single point.

```py
Syntax: Line.are_concurrent(lines)

Parameters:
 lines: a sequence of linear entities.

Returns:
 True:  if the set of linear entities intersect in one point
 False: otherwise.
```

**示例#1:**

```py
# import sympy and Point, Line
from sympy import Point, Line

p1, p2 = Point(0, 0), Point(3, 5)
p3, p4 = Point(-2, -2), Point(0, 2)

l1, l2, l3 = Line(p1, p2), Line(p1, p3), Line(p1, p4)

# using are_concurrent() method
areConcurrent = Line.are_concurrent(l1, l2, l3)

print(areConcurrent)
```

**输出:**

```py
True
```

**示例#2:**

```py
# import sympy and Point, Line
from sympy import Point, Line

p1, p2 = Point(0, 0), Point(3, 5)
p3, p4 = Point(-2, -2), Point(0, 2)

l1, l2, l3 = Line(p1, p3), Line(p1, p4), Line(p2, p3)

# using are_concurrent() method
areConcurrent = Line.are_concurrent(l1, l2, l3)

print(areConcurrent)
```

**输出:**

```py
False
```