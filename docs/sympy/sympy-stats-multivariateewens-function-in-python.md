# Python 中的 sympy . stats . multi variablewens()函数

> 原文:[https://www . geesforgeks . org/sympy-stats-multi variatewens-function-in-python/](https://www.geeksforgeeks.org/sympy-stats-multivariateewens-function-in-python/)

借助于**方法，我们可以创建一个具有多变量 Ewens 分布的离散随机变量。**

```py
**Syntax:** sympy.stats.MultivariateEwens(syms, n, theta)

**Parameters:**
 **syms:** the symbol
 **n:** size of the sample or the integer whose partitions are considered, a positive integer
 **theta:** mutation rate, must be positive real number

**Returns:** a discrete random variable with Multivariate Ewens Distribution. 
```

**例 1 :**

## 蟒 3

```py
# import sympy, MultivariateEwens, density, Symbol
from sympy.stats.joint_rv_types import MultivariateEwens
from sympy.stats import density
from sympy import Symbol, pprint

a = Symbol('a', positive = True)
b = Symbol('b', positive = True)

# using sympy.stats.MultivariateEwens() method
E = MultivariateEwens('E', 2, 1)
mveDist = density(E)(a, b)

pprint(mveDist)
```