# Python–Sympy 多边形. cut_section()方法

> 原文:[https://www . geesforgeks . org/python-sympy-polygon-cut _ section-method/](https://www.geeksforgeeks.org/python-sympy-polygon-cut_section-method/)

在 Sympy 中，函数 **Polygon.cut_section()** 用于获得分别位于交线上方和下方的两个多边形段(多边形的两部分)的元组。它只是返回与直线相交的多边形的两个部分。当线上方或线下方不存在多边形时，返回“无”。

```py
Syntax: Polygon.cut_section(line)

Returns: upper_polygon, lower_polygon: Polygon objects or None
 upper_polygon: is the polygon that lies above the given line
 lower_polygon: is the polygon that lies below the given line
 None: when no polygon exists above the line or below the line

Raises: 
 ValueError: When the line does not intersect the polygon

```

**示例#1:**

## 蟒蛇 3

```py
# import sympy import Point, Polygon, Line
from sympy import Point, Polygon, Line

# creating points using Point()
p1, p2, p3, p4 = map(Point, [(0, 2), (0, 0), (1, 0), (1, 2)])

# creating polygon using Polygon()
poly = Polygon(p1, p2, p3, p4)

# using cut_section()
cutSection = poly.cut_section(Line((0, 1), slope = 0))

print(cutSection)
```

**输出:**

```py
(Polygon(Point2D(0, 2), Point2D(0, 1), Point2D(1, 1), Point2D(1, 2)), 
 Polygon(Point2D(0, 1), Point2D(0, 0), Point2D(1, 0), Point2D(1, 1)))

```

**例 2:**

## 蟒蛇 3

```py
# import sympy import Point, Polygon, Line
from sympy import Point, Polygon, Line

# creating points using Point()
p1, p2, p3, p4 = map(Point, [(0, 2), (0, 0), (1, 0), (1, 2)])

# creating polygon using Polygon()
poly = Polygon(p1, p2, p3, p4)

# using cut_section()
cutSection = poly.cut_section(Line((0, 1), slope = 1))

print(cutSection)
```

**输出:**

```py
(Triangle(Point2D(0, 2), Point2D(0, 1), Point2D(1, 2)), 
 Polygon(Point2D(0, 1), Point2D(0, 0), Point2D(1, 0), Point2D(1, 2)))
```