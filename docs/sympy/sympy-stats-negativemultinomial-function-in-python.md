# Python 中的 sympy . stats . negative emulatinornial()函数

> 原文:[https://www . geeksforgeeks . org/sympy-stats-negative emuletinorial-function-in-python/](https://www.geeksforgeeks.org/sympy-stats-negativemultinomial-function-in-python/)

借助**方法，我们可以创建一个具有负多项式分布的离散随机变量。**

```
**Syntax:** sympy.stats.NegativeMultinomial(syms, k, p)

**Parameters:** 
 **syms:** the symbol
 **k:** number of failures before the experiment is stopped, a positive integer
 **p:** event probabilites, p>= 0 and p<= 1

**Returns:** a discrete random variable with Negative Multinomial Distribution.
```

**例 1 :**

## 蟒 3

```
# import sympy, NegativeMultinomia, density, symbols
from sympy.stats import density
from sympy.stats.joint_rv_types import NegativeMultinomial
from sympy import symbols, pprint

p1, p2, p3 = symbols('p1, p2, p3', positive = True)
x1, x2, x3 = symbols('x1, x2, x3', nonnegative = True, integer = True)

# using sympy.stats.NegativeMultinomial() method
N = NegativeMultinomial('N', 3, p1, p2, p3)
negMulti = density(N)(x1, x2, x3)

pprint(negMulti)
```