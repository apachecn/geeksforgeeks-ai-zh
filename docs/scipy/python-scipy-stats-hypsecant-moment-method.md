# Python | Scipy stats . hyp secant . moment()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-moment-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-moment-method/)

借助`**stats.hypsecant.moment()**`方法，利用`stats.hypsecant.moment()`方法可以得到 n 阶非中心矩的值。

> **语法:** `stats.hypsecant.moment(n, beta)`
> **返回:**返回非中心时刻的值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.hypsecant.moment()`方法，我们能够通过使用这个方法得到非中心矩的值。

```
# import hypsecant
from scipy.stats import hypsecant
beta = 1

# Using stats.hypsecant.moment() method
gfg = hypsecant.moment(3, beta)

print(gfg)
```

**输出:**

> 8.402203300817018

**例 2 :**

```
# import hypsecant
from scipy.stats import hypsecant
beta = 4

# Using stats.hypsecant.moment() method
gfg = hypsecant.moment(4, beta)

print(gfg)
```

**输出:**

> 523.3108465742703