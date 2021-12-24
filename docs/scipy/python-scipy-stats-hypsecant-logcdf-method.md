# Python | Scipy stats . hyp secant . logcdf()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-logcdf-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-logcdf-method/)

借助`**stats.hypsecant.logcdf()**`方法，利用`stats.hypsecant.logcdf()`方法可以得到累积分布函数的对数值。

> **语法:** `stats.hypsecant.logcdf(x, beta)`
> **返回:**返回累计分布函数的对数值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`stats.hypsecant.logcdf()`方法，我们能够使用该方法获得累积分布函数的对数值。

```
# import hypsecant
from scipy.stats import hypsecant
beta = 1

# Using stats.hypsecant.logcdf() method
gfg = hypsecant.logcdf(0.3, beta)

print(gfg)
```

**输出:**

> -1.22613058307804

**例 2 :**

```
# import hypsecant
from scipy.stats import hypsecant
beta = 4

# Using stats.hypsecant.logcdf() method
gfg = hypsecant.logcdf(0.9, beta)

print(gfg)
```

**输出:**

> -3.5522585879999213