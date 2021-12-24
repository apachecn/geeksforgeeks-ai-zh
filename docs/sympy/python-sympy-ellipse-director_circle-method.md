# Python | Sympy 椭圆. director_circle()方法

> 原文:[https://www . geesforgeks . org/python-sympy-ellipse-director _ circle-method/](https://www.geeksforgeeks.org/python-sympy-ellipse-director_circle-method/)

In Sympy, the function `director_circle()` returns a Circle consisting of all points where two perpendicular tangent lines to the ellipse cross each other.

```py
Syntax: Ellipse.director_circle()

Returns: Circle
 A director circle returned as a geometric object.

```

**示例#1:**

```py
# import sympy and Circle, Ellipse, Point
from sympy import Circle, Ellipse, Point

p = Point(3, 8)

# using director_circle() method
directorCircle = Ellipse(p, 7, 9).director_circle()

print(directorCircle)
```

**输出:**

```py
Circle(Point2D(3, 8), sqrt(130))
```

**例 2:**

```py
# import sympy and Circle, Ellipse, Point, symbols
from sympy import Circle, Ellipse, Point, symbols

p = Point(3, 8)
a, b = symbols('a b')

# using director_circle() method
directorCircle = Ellipse(p, a, b).director_circle()

print(directorCircle)
```

**输出:**

```py
Circle(Point2D(3, 8), sqrt(a**2 + b**2))
```