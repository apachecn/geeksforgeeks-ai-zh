# python 中的 sympy . integrations . rational tools . ratint _ log part()

> 原文:[https://www . geeksforgeeks . org/sympy-integrations-rational tools-ratint _ log part-in-python/](https://www.geeksforgeeks.org/sympy-integrals-rationaltools-ratint_logpart-in-python/)

借助 **ratint_logpart()** 方法，利用该方法实现 Lazard Rioboo Trager 算法，可以对不定有理函数进行积分，并返回积分多项式。

> **语法:** ratint_logpart(f，g，x，t=None)
> 
> **返回:**返回综合功能。

**示例#1 :**

在这个例子中我们可以看到，通过使用 **ratint_logpart()** 方法，我们能够使用 Lazard Rioboo Trager 算法计算不定有理积分。

## 蟒蛇 3

```
# import ratint_logpart
from sympy.integrals.rationaltools import ratint_logpart
from sympy.abc import x
from sympy import Poly

# Using ratint_logpart() method
gfg = ratint_logpart(Poly(1, x, domain='ZZ'), 
                     Poly(x*2 + x + 1, x, domain='ZZ'), x)

print(gfg)
```

**输出:**

> [(Poly(3*x + 1，x，domain='ZZ ')，Poly(-3*_t + 1，_t，domain = ' ZZ ')]

**例 2 :**

## 蟒蛇 3

```
# import ratint_logpart
from sympy.integrals.rationaltools import ratint_logpart
from sympy.abc import x, y
from sympy import Poly

# Using ratint_logpart() method
gfg = ratint_logpart(Poly(10, y, domain='ZZ'), 
               Poly(y**2 - 3*y - 2, y, domain='ZZ'), y)

print(gfg)
```

**输出:**

> [(Poly(y–17 * _t/20–3/2，y，domain='QQ[_t]')，Poly(-17*_t**2 + 100，_ t，domain = ' ZZ ')]