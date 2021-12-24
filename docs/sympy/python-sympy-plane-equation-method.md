# Python | Sympy Plane.equation()方法

> 原文:[https://www . geesforgeks . org/python-sympy-plane-equation-method/](https://www.geeksforgeeks.org/python-sympy-plane-equation-method/)

In Simpy, the function `Plane.equation()` is used to make equation of a given Plane.

```py
Syntax :  Plane.equation(x, y, z)

Parameters :
x :  optional
y :  optional
z :  optional

Returns : Equation of Plane

```

**示例#1:**

```py
# import sympy, Point3D and Plane
from sympy import Point3D, Plane

# using Plane()

p1 = Plane(Point3D(1, 2, 3), Point3D(4, 5, 6), Point3D(0, 2, 0))
p2 = p1.equation()

print(p2)
```

**输出:**

```py
-9*x + 6*y + 3*z - 12
```

**示例#2:**

```py
# import sympy, Point3D and Plane
from sympy import Point3D, Plane

# using Plane()

p3 = Plane(Point3D(1, 2, 3), normal_vector =(2, 2, 2))
p4 = p3.equation()

print(p4)
```

**输出:**

```py
2*x + 2*y + 2*z - 12
```