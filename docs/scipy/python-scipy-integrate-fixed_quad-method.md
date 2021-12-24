# Python | Scipy integrate . fixed _ quad()方法

> 原文:[https://www . geesforgeks . org/python-scipy-integrate-fixed _ quad-method/](https://www.geeksforgeeks.org/python-scipy-integrate-fixed_quad-method/)

借助于`**scipy.integrate.fixed_quad()**`方法，我们可以利用`scipy.integrate.fixed_quad()`方法，利用固定阶高斯求积得到定积分的计算。

> **语法:** `scipy.integrate.fixed_quad(func, a, b, n)`
> **返回:**返回定积分的计算值。

**例#1 :**
在这个例子中我们可以看到，通过使用`scipy.integrate.fixed_quad()`方法，我们能够通过使用该方法使用固定阶高斯求积得到定积分。

```py
# import scipy.integrate
from scipy import integrate
func = lambda x: x**3

# using scipy.integrate.fixed_quad() method
gfg = integrate.fixed_quad(func, 0.0, 1.0, n = 2) # n is the order of integration

print(gfg)
```

**输出:**

> 0.24999999999999997

**例 2 :**

```py
# import scipy.integrate
from scipy import integrate
func = lambda x: x**2 + 4 * x + 4

# using scipy.integrate.fixed_quad() method
gfg = integrate.fixed_quad(func, 1.0, 2.0, n = 2) # n is the order of integration

print(gfg)
```

**输出:**

> 12.333333333333332