# Python | Scipy integrate . TPL quad()方法

> 原文:[https://www . geesforgeks . org/python-scipy-integrate-TPL quad-method/](https://www.geeksforgeeks.org/python-scipy-integrate-tplquad-method/)

借助`**scipy.integrate.tplquad()**`方法，利用`scipy.integrate.tplquad()`方法可以得到给定函数从极限 a 到极限 b 的三重积分。

> **语法:** `scipy.integrate.tplquad(func, a, b)`
> 
> **返回:**返回多项式的三重积分值。

**例#1 :**
在这个例子中我们可以看到，通过使用`scipy.integrate.tplquad()`方法，我们能够利用这个方法得到一个多项式从极限 a 到极限 b 的三重积分值。

```
# import scipy.integrate.tplquad
from scipy import integrate

gfg = lambda z, y, x: x * y*z + x**2 + y**2 + z**2

# using scipy.integrate.tplquad() method
geek = integrate.tplquad(gfg, 1, 3, lambda x: 2, lambda x: 3,
                              lambda x, y: 0, lambda x, y: 1)

print(geek)
```

**输出:**

> 27.000000000000004

**例 2 :**

```
# import scipy.integrate.tplquad
from scipy import integrate
gfg = lambda z, y, x: x**2 + y**2 + z**2 + 1

# using scipy.integrate.tplquad() method
geek = integrate.tplquad(gfg, 1, 3, lambda x: 2, lambda x: 3,
                              lambda x, y: 0, lambda x, y: 1)

print(geek)
```

**输出:**

> Twenty-four