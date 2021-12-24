# Python | Scipy stats . hyp secant . PPF()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-PPF-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-ppf-method/)

借助`**stats.hypsecant.ppf()**`方法，我们可以利用`stats.hypsecant.ppf()`方法得到百分点函数的值，即**逆(cdf )** 。

> **语法:** `stats.hypsecant.ppf(x, beta)`
> **返回:**返回百分点函数的值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`stats.hypsecant.ppf()`方法，我们能够使用该方法获得百分点函数的值。

```
# import hypsecant
from scipy.stats import hypsecant
beta = 1

# Using stats.hypsecant.ppf() method
gfg = hypsecant.ppf(0.3, beta)

print(gfg)
```

**输出:**

> 0.3257245223731834

**例 2 :**

```
# import hypsecant
from scipy.stats import hypsecant
beta = 4

# Using stats.hypsecant.ppf() method
gfg = hypsecant.ppf(0.9, beta)

print(gfg)
```

**输出:**

> 5.842730034701113