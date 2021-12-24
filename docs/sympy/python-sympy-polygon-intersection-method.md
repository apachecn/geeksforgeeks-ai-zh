# Python–多边形相交()方法

> 原文:[https://www . geesforgeks . org/python-sympy-polygon-交集-method/](https://www.geeksforgeeks.org/python-sympy-polygon-intersection-method/)

在 Sympy 中，函数**多边形.交集()**用于获取给定多边形与给定几何实体的交集。几何图元可以是点、线、多边形或其他几何图形。如果多边形和给定的几何图元在任何地方都没有相交，则交点可能为空。但是如果存在交点，可以包含单个点或完整的线段。

```py
Syntax: Polygon.intersection(o)

Parameters: Geometry Entity

Returns: The list of Segments or Points of intersection.

```

**例 1:**

## 蟒 3

```py
# import Point, Polygon
from sympy import Point, Polygon

# creating points using Point()
p1, p2, p3, p4 = map(Point, [(0, 0), (1, 0), (5, 1), (0, 1)])
p5, p6, p7 = map(Point, [(3, 2), (1, -1), (0, 2)])

# creating polygons using Polygon()
poly1 = Polygon(p1, p2, p3, p4)
poly2 = Polygon(p5, p6, p7)

# using intersection()
isIntersection = poly1.intersection(poly2)

print(isIntersection)
```