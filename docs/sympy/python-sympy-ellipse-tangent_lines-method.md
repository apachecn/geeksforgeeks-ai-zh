# Python | Sympy 椭圆.切线 _ 直线法

> 原文:[https://www . geesforgeks . org/python-sympy-ellipse-tangent _ lines-method/](https://www.geeksforgeeks.org/python-sympy-ellipse-tangent_lines-method/)

In Sympy, the function `tangent_lines()` returns Tangent lines between p(point) and the ellipse.If p is on the ellipse, returns the tangent line through point p. Otherwise, returns the tangent line(s) from p to the ellipse, or None if no tangent line is possible (e.g., p inside ellipse).

```
Syntax: Ellipse.tangent_lines(p)

Parameter: 
 p:Point

Returns:
 tangent_lines: list with 1 or 2 Lines or empty list

Raises:
 NotImplementedError: Can only find tangent lines for a point, p, on the ellipse.

```

**示例#1:**

```
# import sympy and Point, Ellipse
from sympy import Point, Ellipse

# using Ellipse() method
e1 = Ellipse(Point(0, 0), 3, 2)

# using tangent_lines() method
l1 = e1.tangent_lines(Point(3, 0))

print(l1)
```

**输出:**

```
[Line2D(Point2D(3, 0), Point2D(3, -12))]
```

**示例#2:**

```
# import sympy and Point, Ellipse
from sympy import Point, Ellipse

# using Ellipse() method
e2 = Ellipse(Point(0, 0), 3, 2)

# using tangent_lines() method
l2 = e2.tangent_lines(Point(1, 1))

print(l2)
```

**输出:**

```
[]
```