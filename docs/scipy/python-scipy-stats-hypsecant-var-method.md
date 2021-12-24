# Python | Scipy stats . hyp secant . var()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-var-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-var-method/)

借助`**stats.hypsecant.var()**`方法，我们可以利用`stats.hypsecant.var()`方法得到分布的方差值。

> **语法:** `stats.hypsecant.var(beta)`
> **返回:**返回分布的方差值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.hypsecant.var()`方法，我们能够利用这个方法得到分布的方差值。

```py
# import hypsecant
from scipy.stats import hypsecant
beta = 10

# Using stats.hypsecant.var() method
gfg = hypsecant.var(beta)

print(gfg)
```

**输出:**

> 2.4674011002723395

**例 2 :**

```py
# import hypsecant
from scipy.stats import hypsecant
beta = 30

# Using stats.hypsecant.var() method
gfg = hypsecant.var(beta)

print(gfg)
```

**输出:**

> 2.4674011002723395