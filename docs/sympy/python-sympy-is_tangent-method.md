# Python | Sympy is_tangent()方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ tangent-method/](https://www.geeksforgeeks.org/python-sympy-is_tangent-method/)

在 Sympy 中，函数`is_tangent()`用于检查给定直线是否与给定圆相切。

```
Syntax:  Circle().is_tangent(line)

Return: True:if line is tangent to circle, otherwise False.

```

**示例#1:**

```
# import sympy and geometry module
from sympy import * 
from sympy.geometry import * 

x = Point(0, 0)

# making line with given points
l = Line(Point(5, -5), Point(5, 5))

# making circle with Circle() of 
# radius 5 and using is_tangent()
isTangent = Circle(x, 5).is_tangent(l)

print(isTangent)
```

**输出:**

```
True
```

**例 2:**

```
# import sympy and geometry module
from sympy import * 
from sympy.geometry import * 

x = Point(0, 0)
y = Point(1, 1)

# making line with given points
l = Line(x, y)

# making circle with Circle() of radius 5 and using is_tangent()
isTangent = Circle(x, 5).is_tangent(l)

print(isTangent)
```

**输出:**

```
False
```