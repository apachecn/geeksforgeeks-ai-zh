# Python | synpy plane . is _ 共面()方法

> 原文:[https://www . geesforgeks . org/python-sympy-plane-is _ 共面-method/](https://www.geeksforgeeks.org/python-sympy-plane-is_coplanar-method/)

In Simpy, the function `Plane.is_coplanar()` is used to check whether the given planes are coplanar or not.

```py
Syntax: Plane.is_coplanar(p)

Parameter:
 p: a Plane

Returns:
 True: if planes are coplanar, else False

```

**示例#1:**

```py
# import sympy, Point3D and Plane
from sympy import Point3D, Plane

o = (0, 0, 0)

# using Plane() 
p1 = Plane(o, (1, 1, 1))
p2 = Plane(o, (2, 2, 2))

# using is_coplanar()
isCoplanar = p1.is_coplanar(p2)

print(isCoplanar)
```

**输出:**

```py
True
```

**示例#2:**

```py
# import sympy, Point3D and Plane
from sympy import Point3D, Plane

o = (0, 0, 0)

# using Plane() 
p3 = Plane(o, (1, 1, 1))
p4 = Plane(o, (3, 2, 1))

# using is_coplanar()
isCoplanar = p3.is_coplanar(p4)

print(isCoplanar)
```

**输出:**

```py
False
```