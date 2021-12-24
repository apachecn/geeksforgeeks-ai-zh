# Python | Scipy stats . hyp secant . stats()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-stats-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-stats-method/)

借助`**stats.hypsecant.stats()**`方法，我们可以通过使用`stats.hypsecant.stats()`方法获得均值(' m ')、方差(' v ')、偏斜(' s ')和/或峰度(' k ')的值。

> **语法:** `stats.hypsecant.stats(beta, moments)`
> **返回:**返回均值、方差、偏斜度和峰度的值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`stats.hypsecant.stats()`方法，我们能够使用该方法获得均值、方差、偏斜度和峰度的值。

```py
# import hypsecant
from scipy.stats import hypsecant
beta = 5

# Using stats.hypsecant.stats() method
M, V, S, K = hypsecant.stats(beta, moments ='mvsk')

print(M, V, S, K)
```

**输出:**

> 5.0 2.4674011002723395 0.0 2.0

**例 2 :**

```py
# import hypsecant
from scipy.stats import hypsecant
beta = 3

# Using stats.hypsecant.stats() method
M, V, S, K = hypsecant.stats(beta, moments ='mvsk')

print(M, V, S, K)
```

**输出:**

> 3.0 2.4674011002723395 0.0 2.0