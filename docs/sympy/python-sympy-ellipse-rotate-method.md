# Python | Sympy 椭圆. rotate()方法

> 原文:[https://www . geesforgeks . org/python-sympy-ellipse-rotate-method/](https://www.geeksforgeeks.org/python-sympy-ellipse-rotate-method/)

In Sympy, the function `rotate()` is used to rotate the ellipse counterclockwise about the given point by the given angle.

```
Syntax: Ellipse.rotate(angle=0, pt=None)

Parameters:
angle: in radian
pt: point about which ellipse is rotated in counterclockwise.

Returns: rotated ellipse

```

**示例#1:**

```
# import sympy and pi, Ellipse
from sympy import Ellipse, pi

# using Ellipse() method
e1 = Ellipse((1, 0), 2, 1)

# using rotate() method
e1.rotate(pi / 2)

print(e1)
```

**输出:**

```
Ellipse(Point2D(0, 1), 1, 2)
```

**示例#2:**

```
# import sympy and pi, Ellipse
from sympy import Ellipse, pi

# using Ellipse() method
e2 = Ellipse((1, 0), 2, 1)

# using rotate() with given point method
e2.rotate(pi / 2, (1, 2))

print(e2)
```

**输出:**

```
Ellipse(Point2D(3, 2), 1, 2)
```