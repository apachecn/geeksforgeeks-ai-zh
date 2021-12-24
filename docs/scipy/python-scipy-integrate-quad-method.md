# Python | Scipy integrate.quad()方法

> 原文:[https://www . geesforgeks . org/python-scipy-integrate-quad-method/](https://www.geeksforgeeks.org/python-scipy-integrate-quad-method/)

借助`**scipy.integrate.quad()**`方法，利用`scipy.integrate.quad()`方法可以得到给定函数从极限 a 到极限 b 的积分。

> **语法:** `scipy.integrate.quad(func, a, b)`
> 
> **返回:**返回多项式的积分。

**例#1 :**
在这个例子中我们可以看到，通过使用`scipy.integrate.quad()`方法，我们能够通过使用这个方法得到一个多项式从极限 a 到极限 b 的积分。

```py
# import scipy.integrate.quad
from scipy import integrate
gfg = lambda x: x**2

# using scipy.integrate.quad() method
geek = integrate.quad(gfg, 0, 3)

print(geek)
```

**输出:**

> 9.000000000000002

**例 2 :**

```py
# import scipy.integrate.quad
from scipy import integrate
gfg = lambda x: x**2 + x + 1

# using scipy.integrate.quad() method
geek = integrate.quad(gfg, 1, 4)

print(geek)
```

**输出:**

> Thirty-one point five