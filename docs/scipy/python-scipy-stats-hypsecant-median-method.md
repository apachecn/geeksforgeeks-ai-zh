# Python | Scipy stats.hypsecant .中位数()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-median-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-median-method/)

借助`**stats.hypsecant.median()**`方法，我们可以利用`stats.hypsecant.median()`方法得到分布的中值。

> **语法:** `stats.hypsecant.median(beta)`
> **返回:**返回分布中值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.hypsecant.median()`方法，我们能够利用这个方法得到分布的中值。

```py
# import hypsecant
from scipy.stats import hypsecant
beta = 1

# Using stats.hypsecant.median() method
gfg = hypsecant.median(beta)

print(gfg)
```

**输出:**

> 0.9999999999999999

**例 2 :**

```py
# import hypsecant
from scipy.stats import hypsecant
beta = 4

# Using stats.hypsecant.median() method
gfg = hypsecant.median(beta)

print(gfg)
```

**输出:**

> Four