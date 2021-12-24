# Python | Sympy plane . projection()方法

> 原文:[https://www . geesforgeks . org/python-sympy-plane-projection-method/](https://www.geeksforgeeks.org/python-sympy-plane-projection-method/)

In Sympy, the function `Plane.projection()` is used project the given point onto the given plane along the plane normal which means, the projection is along the normal vector direction of the plane.

```
Syntax:  Plane.projection(pt)

Parameters: 
 pt: Point or Point3D

Returns: Point3D

```

**示例#1:**

```
# import sympy and Plane, Point, Point3D
from sympy import Plane, Point, Point3D

p = Point(2, 2)

# using Plane()
p1 = Plane(Point3D(1, 2, 3), normal_vector =(0, 1, 1))

# using projection()
projectionPoint = p1.projection(p)

print(projectionPoint)
```

**输出:**

```
Point3D(2, 7/2, 3/2)
```

**示例#2:**

```
# import sympy and Plane, Point, Point3D
from sympy import Plane, Point, Point3D

p = Point3D(2, 2, 2)

# using Plane()
p1 = Plane(Point3D(1, 2, 3), normal_vector =(0, 1, 1))

# using projection()
projectionPoint = p1.projection(p)

print(projectionPoint)
```

**输出:**

```
Point3D(2, 5/2, 5/2)
```