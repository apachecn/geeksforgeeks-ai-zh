# Python–Sympy curve . translate()方法

> 原文:[https://www . geesforgeks . org/python-sympy-curve-translate-method/](https://www.geeksforgeeks.org/python-sympy-curve-translate-method/)

In Sympy, the function `Curve.translate()` is used translate the given curve by the given values of x, y. It translates the curve along with both the directions i.e. along x-axis and y-axis.

> **语法:**曲线.平移(x，y)
> 
> **参数:**
> **x:** 沿 x 轴的平移值
> **y:** 沿 y 轴的平移值
> 
> **返回:**平移曲线

**示例#1:**

```
# import Curve, parameter and interpolate
from sympy.geometry.curve import Curve
from sympy.abc import t
from sympy import interpolate

# using interpolate() and Curve()
C1 = Curve((t, interpolate([1, 4, 9, 16], t)), (t, 0, 1));
print(C1)

# using translate()
C2 = C1.translate(2, 3)
print(C2)
```

**输出:**

```
Curve((t, t**2), (t, 0, 1))  
Curve((t + 2, t**2 + 3), (t, 0, 1))

```

**例 2:**

```
# import Curve and parameter
from sympy.geometry.curve import Curve
from sympy.abc import x

# using Curve()
C1 = Curve((x, x), (x, 0, 1));
print(C1)

# using translate()
C2 = C1.translate(1, 2)
print(C2)
```

**输出:**

```
Curve((x, x), (x, 0, 1))  
Curve((x + 1, x + 2), (x, 0, 1))

```