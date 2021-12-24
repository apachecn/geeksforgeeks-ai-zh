# Python | Sympy segment . vertical _ 平分线()方法

> 原文:[https://www . geesforgeks . org/python-sympy-segment-vertical _ 平分线-method/](https://www.geeksforgeeks.org/python-sympy-segment-perpendicular_bisector-method/)

In Sympy, the function `perpendicular_bisector()` is used to find the perpendicular bisector of the given segment. If no point is specified or the point specified is not on the bisector then the bisector is returned as a Line. Otherwise, a Segment is returned that joins the point specified and the intersection of the bisector and the segment.

```
Syntax: Segment.perpendicular_bisector(p=None)

Parameters:
 p: Point

Returns:
 bisector: Line or Segment

```

**示例#1:**

```
# import sympy and Point, Segment
from sympy import Point, Segment

p1, p2, p3 = Point(0, 0), Point(6, 6), Point(5, 1)
s1 = Segment(p1, p2)

# using perpendicular_bisector() method
perpendicularBisector = s1.perpendicular_bisector()

print(perpendicularBisector)
```

**输出:**

```
Line2D(Point2D(3, 3), Point2D(-3, 9))
```

**示例#2:**

```
# import sympy and Point, Segment
from sympy import Point, Segment

p1, p2, p3 = Point(0, 0), Point(6, 6), Point(5, 1)
s1 = Segment(p1, p2)

# using perpendicular_bisector() method
perpendicularBisector = s1.perpendicular_bisector(p3)

print(perpendicularBisector)
```

**输出:**

```
Segment2D(Point2D(5, 1), Point2D(3, 3))
```