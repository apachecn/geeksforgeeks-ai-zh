# Python | Sympy Line.distance()方法

> 原文:[https://www . geesforgeks . org/python-sympy-line-distance-method/](https://www.geeksforgeeks.org/python-sympy-line-distance-method/)

In Sympy, the function `distance()` is used to find the shortest distance between a given line and a given point.

```py
Syntax: Line.distance(other)

Parameter:  
other: a point

Returns: shortest distance between a line and a point

Raises: NotImplementedError is raised if `other` is not a Point

```

**示例#1:**

```py
# import sympy and Point, Line 
from sympy import Point, Line 

p1, p2 = Point(0, 0), Point(1, 1)
s = Line(p1, p2)

# using distance() method
shortestDistance = s.distance(Point(-1, 1))

print(shortestDistance)
```

**输出:**

```py
sqrt(2)
```

**示例#2:**

```py
# import sympy and Point, Line 
from sympy import Point, Line 

p1, p2 = Point(0, 0, 0), Point(1, 1, 1)
s = Line(p1, p2)

# using distance() method
shortestDistance = s.distance(Point(-1, 1, 1))

print(shortestDistance)
```

**输出:**

```py
2*sqrt(6)/3
```