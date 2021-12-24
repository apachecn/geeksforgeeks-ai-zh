# Python | Sympy 椭圆()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-ellipse-method/](https://www.geeksforgeeks.org/python-sympy-ellipse-method/)

In sympy, the function `Ellipse()` is used to create ellipse from a center and two radii, the first being the horizontal radius (along the x-axis) and the second being the vertical radius (along the y-axis).

> **语法:**椭圆()
> 
> **参数:**
> **中心:**点
> **hradius:** 数字或 SymPy 表达式，可选
> **vradius:** 数字或 SymPy 表达式，可选
> **偏心率:**数字或 SymPy 表达式，可选
> 
> **错误:**当 hradius、vradius 和偏心率不正确地作为参数提供时，会引发几何错误；当中心不是点时，会引发类型错误。

**示例#1:使用中心和半径**

```
# import sympy and geometry module 
from sympy.geometry import Point, Ellipse

# using Ellipse()
e1 = Ellipse(Point(0, 0), 5, 1)

print(e1.hradius,e1.vradius)
```

**输出:**

```
(5,1)
```

**例 2:使用中心、半径和偏心**

```
# import sympy and geometry module 
from sympy.geometry import Point, Ellipse, Rational

# using Ellipse()
e2 = Ellipse(Point(3, 1), hradius=3, eccentricity=Rational(4, 5))

print(e2)
```

**输出:**

```
Ellipse(Point2D(3, 1), 3, 9/5)
```

**例#3:使用中心、虚拟和偏心**

```
# import sympy and geometry module 
from sympy.geometry import Point, Ellipse, Rational

# using Ellipse()
e2 = Ellipse(Point(3, 1), vradius=3, eccentricity=Rational(4, 5))

print(e2)
```

**输出:**

```
Ellipse(Point2D(3, 1), 5, 3)
```