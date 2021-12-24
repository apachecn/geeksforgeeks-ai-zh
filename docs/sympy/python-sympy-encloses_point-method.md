# Python | Sympy enclose _ point()方法

> 原文:[https://www . geesforgeks . org/python-sympy-encloss _ point-method/](https://www.geeksforgeeks.org/python-sympy-encloses_point-method/)

In sympy, the function `encloses_point()` is used to check whether the given point is encolsed by given ellipse or not.

```
Syntax: Ellipse.encloses_point(point)

Return: True:if point is enclosed by ellipse, otherwise False.

```

**示例#1:**

```
# import sympy and geometry module 
from sympy import * 
from sympy.geometry import * 

x = Point(0, 0) 

# making ellipse with given point as center and radii
e1 = Ellipse(x, 3, 2)

# using encloses_point() method
isEnclosed = e1.encloses_point((0, 0))

print(isEnclosed)

```

**输出:**

```
True
```

**示例#2:**

```
# import sympy and geometry module 
from sympy import * 
from sympy.geometry import * 

x = Point(3, 1) 

# making ellipse with given point as center, hradius and eccentricity
e2 = Ellipse(x, hradius = 3, eccentricity = Rational(4, 5))

# using encloses_point() method
isEnclosed = e2.encloses_point((4, 6))

print(isEnclosed)

```

**输出:**

```
False
```