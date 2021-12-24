# Python | Scipy integrate . quadrant()方法

> 原文:[https://www . geeksforgeeks . org/python-scipy-integrate-quadration-method/](https://www.geeksforgeeks.org/python-scipy-integrate-quadrature-method/)

借助于`**scipy.integrate.quadrature()**`方法，我们可以通过`scipy.integrate.quadrature()`方法得到采用固定容差高斯求积的定积分的计算。

> **语法:** `scipy.integrate.quadrature(func, a, b)`
> 
> **返回:**将高斯求积近似返回积分。

**例#1 :**
在这个例子中我们可以看到，通过使用`scipy.integrate.quadrature()`方法，我们能够利用这个方法得到积分函数从极限 a 到极限 b 的高斯求积逼近。

```py
# import scipy.integrate.
from scipy import integrate

gfg = lambda x: x**8 + x**4

# using scipy.integrate.quadrature() method
geek = integrate.quadrature(gfg, 0.0, 1.8)

print(geek)
```

**输出:**

> 25.81905715199999

**例 2 :**

```py
# import scipy.integrate.
from scipy import integrate

gfg = lambda x: x**2 + 2 * x + 4

# using scipy.integrate.quadrature() method
geek = integrate.quadrature(gfg, 0.0, 4.0)

print(geek)
```

**输出:**

> 53.33333333333333