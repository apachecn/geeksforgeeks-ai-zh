# Python | Sympy line . interface()方法

> 原文:[https://www . geesforgeks . org/python-sympy-line-intersection-method/](https://www.geeksforgeeks.org/python-sympy-line-intersection-method/)

In Sympy, the function `intersection()` is used to find the intersection with another geometrical entity.

```
Syntax: Line.intersection(o)

Parameters:
 o: Point or LinearEntity

Returns:
 intersection: list of geometrical entities

```

**示例#1:**

```
# import sympy and Point, Line
from sympy import Point, Line

p1, p2, p3 = Point(0, 0), Point(1, 1), Point(7, 7)
l1 = Line(p1, p2)

# using intersection() method
showIntersection = l1.intersection(p3)

print(showIntersection)
```

**输出:**

```
[Point2D(7, 7)]
```

**示例#2:**

```
# import sympy and Point, Line, Segment
from sympy import Point, Line, Segment

p1, p2, p3, p4 = Point(0, 0), Point(1, 1), Point(0, 5), Point(2, 6)
l1 = Line(p1, p2)
s1 = Segment(p3, p4)

# using intersection() method
showIntersection = l1.intersection(s1)

print(showIntersection)
```

**输出:**

```
[]
```