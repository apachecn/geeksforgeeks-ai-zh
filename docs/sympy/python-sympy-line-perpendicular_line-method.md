# Python | Sympy line . vertical _ line 方法

> 原文:[https://www . geesforgeks . org/python-sympy-line-vertical _ line-method/](https://www.geeksforgeeks.org/python-sympy-line-perpendicular_line-method/)

在 Sympy 中，函数 vertical _ Line()用于创建一条垂直于给定线性实体的新直线，该直线穿过给定点 p.

```py
Syntax: Line.perpendicular_line(p)

Parameters:
p: Point

Returns:line 
```

**示例#1:**

## 蟒蛇 3

```py
# import sympy and Point, Line
from sympy import Point, Line

p1, p2, p3 = Point(0, 0), Point(2, 3), Point(-2, 2)

l1 = Line(p1, p2)

# using perpendicular_line() method
l2 = l1.perpendicular_line(p3)

# checking l2 is perpendicular to l1 using is_perpendicular() method
isPerpendicular = l1.is_perpendicular(l2)

print(isPerpendicular)
```

**输出:**

```py
True
```

**例 2:**

## 蟒蛇 3

```py
# import sympy and Point3D, Line3D
from sympy import Point3D, Line3D

p1, p2, p3 = Point3D(0, 0, 0), Point3D(2, 3, 4), Point3D(-2, 2, 0)

l1 = Line3D(p1, p2)

# using perpendicular_line() method
l2 = l1.perpendicular_line(p3)

# checking l2 is perpendicular to l1 using is_perpendicular() method
isPerpendicular = l2 = l1.is_perpendicular(p3)

print(isPerpendicular)
```

**输出:**

```py
True
```