# Python | Scipy stats . half gennorm . stats()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-stats-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-stats-method/)

借助`**stats.halfgennorm.stats()**`方法，我们可以通过使用`stats.halfgennorm.stats()`方法获得均值(' m ')、方差(' v ')、偏斜(' s ')和/或峰度(' k ')的值。

> **语法:** `stats.halfgennorm.stats(beta, moments)`
> **返回:**返回均值、方差、偏斜度和峰度的值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`stats.halfgennorm.stats()`方法，我们能够使用该方法获得均值、方差、偏斜度和峰度的值。

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 5

# Using stats.halfgennorm.stats() method
M, V, S, K = halfgennorm.stats(beta, moments ='mvsk')

print(M, V, S, K)
```

**输出:**

> 0.48317034577918083 0.09092954611981496 0.3281246839804034 -0.754155041309859

**例 2 :**

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 3

# Using stats.halfgennorm.stats() method
M, V, S, K = halfgennorm.stats(beta, moments ='mvsk')

print(M, V, S, K)
```

**输出:**

> 0.5054680881515111 0.1177841857623046 0.6327758514663764 -0.1584840878576932