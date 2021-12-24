# Python | Sympy plane . are _ concurrent()方法

> 原文:[https://www . geesforgeks . org/python-sympy-plane-are _ concurrent-method/](https://www.geeksforgeeks.org/python-sympy-plane-are_concurrent-method/)

In Simpy, the function `Plane.are_concurrent()` is used to check whether the given sequence of planes are concurrent or not. Two or more Planes are concurrent if their intersections are a common line.

```py
Syntax: Plane.are_concurrent()

Parameters:
 planes: sequence of planes

Returns:
 True: if they are concurrent, else False

```

**示例#1:**

```py
# import sympy, Point3D and Plane
from sympy import Point3D, Plane

# using Plane() 
p1 = Plane(Point3D(5, 0, 0), normal_vector =(1, -1, 1))
p2 = Plane(Point3D(0, -2, 0), normal_vector =(3, 1, 1))

# using are_concurrent()
areConcurrent = Plane.are_concurrent(p1, p2)

print(areConcurrent)
```

**输出:**

```py
True
```

**示例#2:**

```py
# import sympy, Point3D and Plane
from sympy import Point3D, Plane

# using Plane() 
p1 = Plane(Point3D(5, 0, 0), normal_vector =(1, -1, 1))
p2 = Plane(Point3D(0, -2, 0), normal_vector =(3, 1, 1))
p3 = Plane(Point3D(0, -1, 0), normal_vector =(5, -1, 9))

# using are_concurrent()
areConcurrent = Plane.are_concurrent(p1, p2, p3)

print(areConcurrent)
```

**输出:**

```py
False
```