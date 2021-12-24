# Python | Sympy Circle()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-circle-method/](https://www.geeksforgeeks.org/python-sympy-circle-method/)

In Simpy, the function `Circle()` is used to make circle from a center and a radius, from three non-collinear points, or the equation of a circle.

> **语法:** `Circle()`
> 
> **参数:**
> **中心**:点和
> **半径**:数或符号表达式或
> **点**:三点序列或
> **方程**:圆的方程
> 
> **误差:**当给定的方程不是圆的方程时，产生几何误差。当试图用不正确的参数构造圆时。

**示例#1:使用中心和半径**

```
# import sympy and geometry module
from sympy.geometry import Point, Circle

# using Circle()
c1 = Circle(Point(0, 0), 5)

print(c1.hradius, c1.vradius, c1.radius)
```

**输出:**

```
(5, 5, 5)
```

**例 2:使用三点序列**

```
# import sympy and geometry module
from sympy.geometry import Point, Circle

# using Circle()
c2 = Circle(Point(0, 0), Point(1, 1), Point(1, 0))

print(c2.hradius, c2.vradius, c2.radius)
```

**输出:**

```
(sqrt(2)/2, sqrt(2)/2, sqrt(2)/2)
```

**例#3:利用圆的方程**

```
# import sympy and geometry module
from sympy.geometry import Point, Circle 
from sympy import Eq

# using Circle()
c3 = Circle(x**2 + y**2 - 25)

print(c3)
```

**输出:**

```
Circle(Point2D(0, 0), 5)
```