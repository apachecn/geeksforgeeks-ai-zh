# Python | Scipy integrate . dbl quad()方法

> 原文:[https://www . geesforgeks . org/python-scipy-integrate-dbl quad-method/](https://www.geeksforgeeks.org/python-scipy-integrate-dblquad-method/)

借助`**scipy.integrate.dblquad()**`方法，利用`scipy.integrate.dblquad()`方法可以得到给定函数从极限 a 到极限 b 的二重积分。

> **语法:** `scipy.integrate.dblquad(func, a, b)`
> 
> **返回:**返回多项式的二重积分值。

**例#1 :**
在这个例子中我们可以看到，通过使用`scipy.integrate.dblquad()`方法，我们能够利用这个方法得到一个多项式从极限 a 到极限 b 的二重积分。

```py
# import scipy.integrate.dblquad
from scipy import integrate

gfg = lambda y, x: x * y**2

# using scipy.integrate.dblquad() method
geek = integrate.dblquad(gfg, 0, 3, lambda x: 0, lambda x: 1)

print(geek)
```

**输出:**

> 1.4999999999999998

**例 2 :**

```py
# import scipy.integrate.dblquad
from scipy import integrate
gfg = lambda y, x: x * y**2 + 2 * x*y + 4

# using scipy.integrate.dblquad() method
geek = integrate.dblquad(gfg, 1, 4, lambda x: 0, lambda x: 1)

print(geek)
```

**输出:**

> 21.999999999999996