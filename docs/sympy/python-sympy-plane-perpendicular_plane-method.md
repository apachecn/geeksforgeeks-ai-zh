# Python | Sympy plane . vertical _ plane()方法

> 原文:[https://www . geesforgeks . org/python-sympy-plane-vertical _ plane-method/](https://www.geeksforgeeks.org/python-sympy-plane-perpendicular_plane-method/)

In Sympy, the function `Plane.perpendicular_plane()` is used to return a perpendicular plane passing through the given points. If the direction ratio between the points is the same as the Plane’s normal vector then, to select from the infinite number of possible planes, a third point will be chosen on the z-axis (or the y-axis if the normal vector is already parallel to the z-axis).

如果给出的点数少于两个，它们将如下提供:如果没有给出点数，那么 pt1 将是自身的。如果没有给出第二个点，它将是在平行于 z 轴的线上通过 pt1 的点(如果法线还不是 z 轴，否则在平行于 y 轴的线上)。

```
Syntax: Plane.perpendicular_plane(pts)

Parameters:
 pts: 0, 1 or 2 Point3D

Returns: Plane

```

**示例#1:**

```
# import sympy, Point3D and Plane, Line3D
from sympy import Point3D, Plane, Line3D

l1, l2 = Point3D(0, 0, 0), Point3D(1, 2, 3)
z1 = (1, 0, 1)

# using Plane()
p1 = Plane(a, normal_vector = z1)

# using perpendicular_plane() with two parameters
perpendicularPlane = p1.perpendicular_plane(l1, l2)

print(perpendicularPlane)
```

**输出:**

```
Plane(Point3D(0, 0, 0), (2, 2, -2))
```

**示例#2:**

```
# import sympy, Point3D and Plane, Line3D
from sympy import Point3D, Plane, Line3D

l3, l4 = Point3D(0, 0, 0), Point3D(1, 1, 0)
z2 = (0, 1, 1)

# using Plane()
p2 = Plane(l3, normal_vector = z2)

# using perpendicular_plane() with one parameter
perpendicularPlane = p2.perpendicular_plane(l4)

print(perpendicularPlane)
```

**输出:**

```
Plane(Point3D(1, 1, 0), (-1, 0, 0))
```