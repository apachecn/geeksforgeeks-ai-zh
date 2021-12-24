# Python | Scipy stats . hyp secant . mean()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-mean-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-mean-method/)

借助`**stats.hypsecant.mean()**`方法，我们可以用`stats.hypsecant.mean()`方法得到分布的平均值。

> **语法:** `stats.hypsecant.mean(beta)`
> **返回:**返回分布均值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.hypsecant.mean()`方法，我们能够通过使用这个方法得到分布的平均值。

```
# import hypsecant
from scipy.stats import hypsecant
beta = 1

# Using stats.hypsecant.mean() method
gfg = hypsecant.mean(beta)

print(gfg)
```

**输出:**

> One

**例 2 :**

```
# import hypsecant
from scipy.stats import hypsecant
beta = 4

# Using stats.hypsecant.mean() method
gfg = hypsecant.mean(beta)

print(gfg)
```

**输出:**

> Four