# Python | Sympy 椭圆.方程()方法

> 原文:[https://www . geesforgeks . org/python-sympy-椭圆-方程-方法/](https://www.geeksforgeeks.org/python-sympy-ellipse-equation-method/)

In sympy, the function `Ellipse.equation()` is used to make the equation of the given ellipse.

```py
Syntax: Ellipse.equation(x='x', y='y', _slope=None)

Parameters:
x : Label for the x-axis. Default value is ‘x’.
y : Label for the y-axis. Default value is ‘y’.
_slope : The slope of the major axis. Ignored when ‘None’.

Returns: equation : sympy expression

```

**示例#1:**

```py
# import sympy, Point and Ellipse
from sympy import Point, Ellipse
from sympy.abc import x, y

# using Ellipse() 
e1 = Ellipse(Point(1, 0), 3, 2)

# using equation()
eq1 = e1.equation(x, y);

print(eq1)
```

**输出:**

```py
y**2/4 + (x/3 - 1/3)**2 - 1
```

**示例#2:**

```py
# import sympy, Point and Ellipse
from sympy import Point, Ellipse
from sympy.abc import x, y

# using Ellipse() 
e2 = Ellipse(Point(0, 0), 3, 2)

# using equation()
eq2 = e2.equation(x, y);

print(eq2)
```

**输出:**

```py
x**2/9 + y**2/4 - 1
```