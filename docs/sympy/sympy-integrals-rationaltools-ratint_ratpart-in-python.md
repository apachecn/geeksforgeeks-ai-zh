# python 中的 sympy . integrations . rational tools . ratint _ rat part()

> 原文:[https://www . geeksforgeeks . org/sympy-integrations-rational tools-ratint _ rat part-in-python/](https://www.geeksforgeeks.org/sympy-integrals-rationaltools-ratint_ratpart-in-python/)

借助 **ratint_ratpart()** 方法，我们可以实现霍洛维茨奥斯特罗格拉茨基算法，它将使用该方法返回分数 A 和 B。

> **语法:** ratint_ratpart(f，g，x)
> 
> **返回:**返回分数 A 和分数 b

**示例#1 :**

在这个例子中，我们可以看到，通过使用 **ratint_ratpart()** 方法，我们能够使用霍洛维茨奥斯特罗格拉茨基算法计算有理积分，并返回分数 A 和 b

## 蟒蛇 3

```
# import ratint_ratpart
from sympy.integrals.rationaltools import ratint_ratpart
from sympy.abc import x, y
from sympy import Poly

# Using ratint_ratpart() method
gfg = ratint_ratpart(Poly(5, x, domain='ZZ'), Poly(x**4 + 1, x, domain='ZZ'), x)

print(gfg)
```

**输出:**

> (0，5/(x**4 + 1))

**例 2 :**

## 蟒蛇 3

```
# import ratint_ratpart
from sympy.integrals.rationaltools import ratint_ratpart
from sympy.abc import x, y
from sympy import Poly

# Using ratint_ratpart() method
gfg = ratint_ratpart(Poly(13, x, domain='ZZ'), Poly(4*x**2 + x - 2, x, domain='ZZ'), x)

print(gfg)
```

**输出:**

> (0，13/(4 * x * * 2+x–2))