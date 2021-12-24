# 症状统计。Python 中的 wigner 半圆()

> 原文:[https://www . geesforgeks . org/sympy-stats-wigner 半圆-in-python/](https://www.geeksforgeeks.org/sympy-stats-wignersemicircle-in-python/)

借助`**sympy.stats.WignerSemicircle()**`方法，我们可以得到代表维格纳半圆分布的连续随机变量。

![](img/0c16f1c7e229e9c875b1dced2514466b.png)

> **句法:** `sympy.stats.WignerSemicircle(name, R)`
> 其中，R 为实数。
> **返回:**返回连续随机变量。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.stats.WignerSemicircle()`方法，我们能够通过使用该方法获得表示 Wigner 半圆分布的连续随机变量。

```
# Import sympy and WignerSemicircle
from sympy.stats import WignerSemicircle, density
from sympy import Symbol, pprint

z = Symbol("z")
r = Symbol("r", positive = True)

# Using sympy.stats.WignerSemicircle() method
X = WignerSemicircle("x", r)
gfg = density(X)(z)

pprint(gfg)
```

**输出:**

> _ _ _ _ _
> /2 2
> 2 * \/r–z
> ——
> 2
> pi * r

**例 2 :**

```
# Import sympy and WignerSemicircle
from sympy.stats import WignerSemicircle, density
from sympy import Symbol, pprint

z = 0.87
r = 2

# Using sympy.stats.WignerSemicircle() method
X = WignerSemicircle("x", r)
gfg = density(X)(z)

pprint(gfg)
```

**输出:**

> 0.900430452616969
> —————
> pi