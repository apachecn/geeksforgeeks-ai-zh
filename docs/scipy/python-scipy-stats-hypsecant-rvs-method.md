# Python | Scipy stats . hyp secant . RVs()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-RVs-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-rvs-method/)

借助于`**stats.hypsecant.rvs()**`方法，我们可以用`stats.hypsecant.rvs()`方法由双曲广义正态分布生成随机变量。

> **语法:** `stats.hypsecant.rvs(beta)`
> **返回:**返回随机变量的值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.hypsecant.rvs()`方法，我们能够利用这个方法得到双曲广义正态分布的随机变量。

```py
# import hypsecant
from scipy.stats import hypsecant
beta = 1

# Using stats.hypsecant.rvs() method
gfg = hypsecant.rvs(beta)

print(gfg)
```

**输出:**

> 0.40565844121963746

**例 2 :**

```py
# import hypsecant
from scipy.stats import hypsecant
beta = 4

# Using stats.hypsecant.rvs() method
gfg = hypsecant.rvs(beta)

print(gfg)
```

**输出:**

> 5.488580336624199