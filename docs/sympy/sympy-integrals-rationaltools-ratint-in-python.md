# python 中的 symy . integrations . rational tools . ratint()

> 原文:[https://www . geeksforgeeks . org/sympy-integrations-rational tools-ratint-in-python/](https://www.geeksforgeeks.org/sympy-integrals-rationaltools-ratint-in-python/)

借助 **ratint()** 方法，我们可以计算一个有理函数的不定积分。如果一个函数是一个有理函数，那么它们就是用这种方法实现的拉扎德·里奥布·特雷格和霍洛维茨·奥斯特罗格拉茨基算法。

> **语法:** ratint(f，x，**flags)
> 
> **返回:**返回综合功能。

**示例#1 :**

在这个例子中，我们可以看到，通过使用 **ratint()** 方法，我们能够计算有理函数的不定积分，并通过使用该方法返回积分函数。

## 蟒蛇 3

```py
# import ratint
from sympy.integrals.rationaltools import ratint
from sympy.abc import x

# Using ratint() method
gfg = ratint((x**5 - 2*x**3 + x - 2)/12, x)

print(gfg)
```

**输出:**

> x * * 6/72–x * * 4/24+x * * 2/24–x/6

**例 2 :**

## 蟒蛇 3

```py
# import ratint
from sympy.integrals.rationaltools import ratint
from sympy.abc import y

# Using ratint() method
gfg = ratint((3*y**3 + 4*x**2 + y - 2), y)

print(gfg)
```

**输出:**

> 3 * y * * 4/4+y * * 2/2+y *(4 * x * * 2–2)