# Python–Sympy 多边形. is _ 凸()方法

> 原文:[https://www . geesforgeks . org/python-sympy-polygon-is _ 凸-method/](https://www.geeksforgeeks.org/python-sympy-polygon-is_convex-method/)

在 Sympy 中，函数**polygon . is _ 凸()**用于检查给定的多边形是否凸。如果一个多边形的所有内角都小于 180 度，并且边之间没有交点，那么这个多边形就是凸的。

```
Syntax: Polygon.is_convex()

Returns:
 True: True if this polygon is convex, False otherwise.

```

**示例#1:**

## 蟒蛇 3

```
# import Point, Polygon
from sympy import Point, Polygon

# creating points using Point()
p1, p2, p3, p4 = map(Point, [(0, 0), (1, 0), (5, 1), (0, 1)])

# creating polygon using Polygon()
isConvex = Polygon(p1, p2, p3, p4)

# using is_convex()
print(isConvex.is_convex())
```

**输出:**

```
True
```

**例 2:**

## 蟒蛇 3

```
# import Point, Polygon
from sympy import Point, Polygon

# creating points using Point()
p1, p2, p3, p4, p5 = map(Point, [(0, 0), (3, 2), (4, 5), (7, 1), (6, 3)])

# creating polygon using Polygon()
isConvex = Polygon(p1, p2, p3, p4, p5)

# using is_convex()
print(isConvex.is_convex())
```

**输出:**

```
False
```