# Python | Scipy stats . hyp secant . CDF()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-CDF-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-cdf-method/)

借助`**stats.hypsecant.cdf()**`方法，我们可以利用`stats.hypsecant.cdf()`方法得到累积分布函数值。

> **语法:** `stats.hypsecant.cdf(x, beta)`
> **返回:**返回累计分布函数值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.hypsecant.cdf()`方法，我们能够通过使用这个方法得到累积分布函数值。

```
# import hypsecant
from scipy.stats import hypsecant
beta = 1

# Using stats.hypsecant.cdf() method
gfg = hypsecant.cdf(0.3, beta)

print(gfg)
```

**输出:**

> 0.29342577051097424

**例 2 :**

```
# import hypsecant
from scipy.stats import hypsecant
beta = 4

# Using stats.hypsecant.cdf() method
gfg = hypsecant.cdf(0.9, beta)

print(gfg)
```

**输出:**

> 0.028659835738036286