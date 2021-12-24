# Python 中的 sympy.stats.MultivariateT()函数

> 原文:[https://www . geesforgeks . org/sympy-stats-multi variatet-function-in-python/](https://www.geeksforgeeks.org/sympy-stats-multivariatet-function-in-python/)

借助**方法，我们可以创建一个具有多元 T 分布的联合随机变量。**

```
**Syntax:** sympy.stats.MultivariateT(syms, mu, sigma, v)

**Parameters:**
 **syms:** the symbol for identifying the random variable
 **mu:** a matrix representing the location vector
 **sigma:** The shape matrix for the distribution
 **v: a** real number

**Returns:** a joint random variable with multivariate T-distribution. 
```

**例 1 :**

## 蟒 3

```
# import sympy, MultivariateT, density, Symbol
from sympy.stats import density, MultivariateT
from sympy import Symbol, pprint

x = Symbol("x")

# using sympy.stats.MultivariateT() method
X = MultivariateT("x", [1, 1], [[1, 0], [0, 1]], 2)
multiVar = density(X)(1, 2)

pprint(multiVar)
```