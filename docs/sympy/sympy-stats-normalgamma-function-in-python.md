# Python 中的 sympy.stats.NormalGamma()函数

> 原文:[https://www . geeksforgeeks . org/sympy-stats-normal gamma-python 中的函数/](https://www.geeksforgeeks.org/sympy-stats-normalgamma-function-in-python/)

借助于**方法，我们可以创建一个具有多元正态伽马分布的二元联合随机变量。**

```
**Syntax: ** sympy.stats.NormalGamma(syms, mu, lamda, alpha, beta)

**Parameters:**
 **syms:** the symbol, for identifying the random variable
 **mu:** a real number, the mean of the normal distribution
 **lambda:** a positive integer
 **alpha:** a positive integer
 **beta:** a positive integer

**Returns: ** a bivariate joint random variable with multivariate Normal gamma distribution. 
```

**例 1 :**

## 蟒 3

```
# import sympy, NormalGamma, density, symbols
from sympy.stats import density, NormalGamma
from sympy import symbols, pprint

y, z = symbols('y z')

# using sympy.stats.NormalGamma() method
X = NormalGamma('X', 0, 1, 2, 3)
norGammaDist = density(X)(y, z)

pprint(norGammaDist)
```