# python 中的辛.积分.变换.逆 _hankel_transform()

> 原文:[https://www . geeksforgeeks . org/sympy-integrations-transforms-inverse _ Hankel _ transform-in-python/](https://www.geeksforgeeks.org/sympy-integrals-transforms-inverse_hankel_transform-in-python/)

借助**逆汉克尔变换()**方法，我们可以计算汉克尔变换的逆，并使用该方法返回未赋值的函数。

![](img/096da684451ac89789f792de512b8314.png)

逆汉克尔变换

> **语法:**逆 _hankel_transform(F，k，r，nu，* *提示)
> 
> **返回:**返回未赋值函数。

**示例#1 :**

在这个例子中我们可以看到，通过使用**逆汉克尔变换()**方法，我们能够计算逆汉克尔变换并返回未赋值的函数。

## 蟒蛇 3

```py
# import inverse_hankel_transform
from sympy import hankel_transform, inverse_hankel_transform, gamma
from sympy import gamma, exp, sinh, cosh
from sympy.abc import r, k, m, nu, a

ht = hankel_transform(5/(r*m), r, k, nu)

# Using inverse_hankel_transform() method
gfg = inverse_hankel_transform(ht, k, r, nu)

print(gfg)
```

**输出:**

> 5/(m*r)

**例 2 :**

## 蟒蛇 3

```py
# import inverse_hankel_transform
from sympy import hankel_transform, inverse_hankel_transform, gamma
from sympy import gamma, exp, sinh, cosh
from sympy.abc import r, k, m, nu, a

ht = hankel_transform(exp(-2*r), r, k, 0)

# Using inverse_hankel_transform() method
gfg = inverse_hankel_transform(ht, k, r, 0)

print(gfg)
```

**输出:**

> exp(-2*r)