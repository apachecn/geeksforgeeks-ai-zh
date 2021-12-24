# Python | Sympy Line .最小 _ 角度 _ 间法

> 原文:[https://www . geesforgeks . org/python-sympy-line-minist _ angle _ between-method/](https://www.geeksforgeeks.org/python-sympy-line-smallest_angle_between-method/)

In Sympy, the function `smallest_angle_between()` is used to return the non-obtuse angle at the intersection of lines.

```py
Syntax: smallest_angle_between(l2)

Parameters: 
 l1: LinearEntity
 l2: LinearEntity

Returns: angle [angle in radians]

```

**示例#1:**

```py
# import sympy and Point, Line, pi
from sympy import Point, Line, pi

# using Line() method
l1 = Line((0, 0), (1, 0))
l2 = Line((1, 1), (0, 0))

# using smallest_angle_between() method
rad = l2.smallest_angle_between(l1)

print(rad)
```

**输出:**

```py
pi/4
```

**示例#2:**

```py
# import sympy and Point, Line, pi
from sympy import Point, Line, pi

# using Line() method
l1 = Line((0, 0), (1, 0))
l3 = Line((3, 1), (0, 0))

# using smallest_angle_between() method
rad = l3.smallest_angle_between(l1)

print(rad)
```

**输出:**

```py
acos(3*sqrt(10)/10)
```