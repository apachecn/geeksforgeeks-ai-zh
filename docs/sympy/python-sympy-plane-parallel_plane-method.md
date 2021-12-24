# Python | Sympy plane . parallel _ plane()方法

> 原文:[https://www . geesforgeks . org/python-sympy-plane-parallel _ plane-method/](https://www.geeksforgeeks.org/python-sympy-plane-parallel_plane-method/)

在 Sympy 中，函数 Plane.parallel_plane()用于返回平行于给定平面并通过给定点的平面。

```py
Syntax: Plane.parallel_plane(pt)

Parameters:
 pt: Point3D

Returns: Plane
```

**示例#1:**

## 蟒蛇 3

```py
# import sympy, Point3D and Plane
from sympy import Point3D, Plane

# using Plane()
p1 = Plane(Point3D(1, 2, 3), normal_vector =(4, 5, 6))

# using parallel_plane()
parallelPlane = p1.parallel_plane(Point3D(2, 3, 5))

print(parallelPlane)
```

**输出:**

```py
Plane(Point3D(2, 3, 5), (4, 5, 6))
```

**例 2:**

## 蟒蛇 3

```py
# import sympy, Point3D and Plane
from sympy import Point3D, Plane

# using Plane()
p2 = Plane(Point3D(1, 1, 2), Point3D(2, 4, 7), Point3D(3, 5, 1))

# using parallel_plane()
parallelPlane = p2.parallel_plane(Point3D(1, 2, 3))

print(parallelPlane)
```

**输出:**

```py
Plane(Point3D(1, 2, 3), (-23, 11, -2))
```