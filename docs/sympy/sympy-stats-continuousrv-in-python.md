# 症状统计。Python 中的 ContinuousRV()

> 原文:[https://www . geesforgeks . org/sympy-stats-continuousrv-in-python/](https://www.geeksforgeeks.org/sympy-stats-continuousrv-in-python/)

借助`**sympy.stats.ContinuousRV()**`方法，我们可以得到代表连续随机变量分布的连续随机变量。

> **语法:** `sympy.stats.ContinuousRV(symbol, density, set=Interval(- oo, oo))`
> 
> **参数:**
> 1)密度–代表概率密度函数。
> 2)设置–表示密度函数有效的原因。
> 
> **返回:**返回连续随机变量。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.stats.ContinuousRV()`方法，我们能够通过使用该方法获得表示连续随机变量分布的连续随机变量。

```
# Import sympy and ContinuousRV
from sympy.stats import ContinuousRV, P, E
from sympy import Symbol, pprint, sqrt

z = Symbol("z")
pdf = sqrt(2)*z / pi

# Using sympy.stats.ContinuousRV() method
X = ContinuousRV(z, pdf)
gfg = density(X)

pprint(gfg)
```

**输出:**

> continuousdistributionhandling(Lambda(z，分片)((sqrt(2)*z/pi，(z >= -oo) &
> (z < oo))、(0，True)))、Interval(-oo，oo))

**例 2 :**

```
# Import sympy and ContinuousRV
from sympy.stats import ContinuousRV, P, E
from sympy import Symbol, pprint, sqrt

z = Symbol("z")
pdf = sqrt(2)*z / pi

# Using sympy.stats.ContinuousRV() method
X = ContinuousRV(z, pdf)

print(P(X>0))
```

**输出:**

> 1/2