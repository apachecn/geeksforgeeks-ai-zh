# Python–Sympy 多边形. distance()方法

> 原文:[https://www . geesforgeks . org/python-sympy-polygon-distance-method/](https://www.geeksforgeeks.org/python-sympy-polygon-distance-method/)

在 Sympy 中，函数 **Polygon.distance()** 用来返回给定多边形与 o 之间的最短距离，如果 o 是一个点，那么给定多边形不需要是凸的。但是如果 o 是另一个多边形，那么给定的多边形和 o 一定是凸的。

```
Syntax: Polygon.distance(o)

Parameters:
 o:Point or Polygon

Returns: the shortest distance between the given polygon and o.
```

**示例#1:**

## 蟒蛇 3

```
# import sympy import Point, Polygon
from sympy import Point, Polygon

# creating points using Point()
p1, p2, p3, p4 = map(Point, [(0, 2), (0, 0), (1, 0), (1, 2)])

# creating polygon using Polygon()
poly = Polygon(p1, p2, p3, p4)

# using distance()
shortestDistance = poly.distance(Point(3, 5))

print(shortestDistance)
```

**输出:**

```
sqrt(13)
```

**例 2:**

## 蟒蛇 3

```
# import sympy import Point, Polygon, RegularPolygon
from sympy import Point, Polygon, RegularPolygon

# creating points using Point()
p1, p2 = map(Point, [(0, 0), (7, 5)])

# creating polygon using Polygon() and RegularPolygon()
poly = Polygon(*RegularPolygon(p1, 1, 3).vertices)

# using distance()
shortestDistance = poly.distance(p2)

print(shortestDistance)
```

**输出:**

```
sqrt(61)
```