# Python 中的 sympy . stats . multivariebeta()函数

> 原文:[https://www . geesforgeks . org/sympy-stats-multivariebeta-function-in-python/](https://www.geeksforgeeks.org/sympy-stats-multivariatebeta-function-in-python/)

借助**sympy . stats . multivariebeta()**方法，我们可以创建一个具有狄利克雷/多元贝塔分布的连续随机变量。

它是β分布的多元推广。

```py
Syntax: sympy.stats.MultivariateBeta(syms, alpha)

Parameters: 
 syms: the symbol
 alpha: positive real numbers signifying concentration numbers

Returns: a continuous random variable with multivariate beta distribution.
```

**示例#1 :**

## 蟒蛇 3

```py
# import sympy, MultivariateBeta, density, Symbol
from sympy.stats.joint_rv_types import MultivariateBeta
from sympy.stats import density
from sympy import Symbol, pprint

a = Symbol('a', positive = True)
b = Symbol('b', positive = True)
x = Symbol('x')
y = Symbol('y')

# using sympy.stats.MultivariateBeta() method
M = MultivariateBeta('M', [a, b])
mvbDist = density(M)(x, y)

pprint(mvbDist)
```

**输出:**

```py
 a1 - 1  a2 - 1               
x      *y      *Gamma(a1 + a2)
------------------------------
     Gamma(a1)*Gamma(a2)     
```

**例 2 :**

## 蟒蛇 3

```py
# import sympy, MultivariateBeta, density, Symbol
from sympy.stats.joint_rv_types import MultivariateBeta
from sympy.stats import density
from sympy import Symbol, pprint

x = Symbol('x')
y = Symbol('y')

# using sympy.stats.MultivariateBeta() method
M = MultivariateBeta('M', [2, 1 / 2])
mvbDist = density(M)(x, y)

pprint(mvbDist)
```

**输出:**

```py
  3*x  
-------
    ___
4*\/ y 
```