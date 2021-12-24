# Python | Sympy 方程()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-equation-method/](https://www.geeksforgeeks.org/python-sympy-equation-method/)

在 Simpy 中，函数`equation()`用于制作给定圆的方程。

```
Syntax : equation(x='x', y='y')

Parameters:
x : str or Symbol, optional
y : str or Symbol, optional

Returns : SymPy expression

```

**例#1:**

```
# import sympy, Point and Circle
from sympy import Point, Circle

# using Circle()
c1 = Circle(Point(0, 0), 5)
c2 = c1.equation()

print(c2)
```

**输出:**

```
x**2 + y**2 - 25
```

**例#2:**

```
# import sympy, Point and Circle
from sympy import Point, Circle

# using Circle()
c3 = Circle(Point(1, 2), 5)
c4 = c3.equation()

print(c4)
```

**输出:**

```
(x - 1)**2 + (y - 2)**2 - 25
```