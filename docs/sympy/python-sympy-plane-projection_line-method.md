# Python | synpy plane . projection _ line()方法

> 原文:[https://www . geesforgeks . org/python-sympy-plane-projection _ line-method/](https://www.geeksforgeeks.org/python-sympy-plane-projection_line-method/)

In Sympy, the function `Plane.projection_line()` is used to project the given line onto the given plane through the normal plane containing the line.

```
Syntax: Plane.projection_line(line)

Parameters:
 line: LinearEntity or LinearEntity3D

Returns: Point3D, Line3D, Ray3D or Segment3D

```

示例#1:

```
# import sympy and Plane, Line, Line3D, Point, Point3D
from sympy import Plane, Line, Line3D, Point, Point3D

p = Line(Point(1, 2), Point(2, 3))

# using Plane()
p1 = Plane(Point3D(1, 2, 3), normal_vector =(1, 0, 1))

# using projection_line()
projectionLine = p1.projection_line(p)

print(projectionLine)
```

**输出:**

```
Line3D(Point3D(5/2, 2, 3/2), Point3D(3, 3, 1))
```

示例 2:

```
# import sympy and Plane, Line, Line3D, Point, Point3D
from sympy import Plane, Line, Line3D, Point, Point3D

p = Line3D(Point3D(1, 2, 3), Point(0, 0, 0))

# using Plane()
p2 = Plane(Point3D(1, 1, 1), normal_vector =(0, 0, 0))

# using projection_line()
projectionLine = p2.projection_line(p)

print(projectionLine)
```

**输出:**

```
Line3D(Point3D(1, 2, 3), Point3D(2, 0, 2))
```