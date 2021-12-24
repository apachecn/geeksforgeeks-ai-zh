# Python | Sympy 椭圆. is_tangent()方法

> 原文:[https://www . geesforgeks . org/python-sympy-ellipse-is _ tangent-method/](https://www.geeksforgeeks.org/python-sympy-ellipse-is_tangent-method/)

In Sympy, the function `Ellipse.is_tangent()` is used to check whether an Ellipse, LinearEntity or Polygon is tangent to the given Ellipse or not.

```py
Syntax: is_tangent(o)

Parameters: o  an Ellipse, LinearEntity or Polygon

Returns: True if o is tangent to the ellipse, False otherwise.

Raises: NotImplementedError When the wrong type of argument is supplied.
```

**示例#1:**

```py
# import sympy and Point, Ellipse, Line
from sympy import Point, Ellipse, Line

p0, p1, p2 = Point(0, 0), Point(3, 0), Point(3, 3)

# using Line and Ellipse method
e1 = Ellipse(p0, 3, 2)
l1 = Line(p1, p2)

# using is_tangent method
e1.is_tangent(l1)
```

**输出:**

```py
True
```

**示例#2:**

```py
# import sympy and Point, Ellipse, Line
from sympy import Point, Ellipse, Line

p0, p1, p2 = Point(0, 0), Point(4, 0), Point(4, 2)

# using Line and Ellipse method
e1 = Ellipse(p0, 3, 2)
l1 = Line(p1, p2)

# using is_tangent method
e1.is_tangent(l1)
```

**输出:**

```py
False
```