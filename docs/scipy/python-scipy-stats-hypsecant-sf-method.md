# Python | Scipy stats .hyps 割线. sf()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-SF-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-sf-method/)

借助`**stats.hypsecant.sf()**`方法，我们可以利用`stats.hypsecant.sf()`方法得到生存函数值为**1–CDF**。

> **语法:** `stats.hypsecant.sf(x, beta)`
> **返回:**返回生存函数的值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.hypsecant.sf()`方法，我们能够通过使用这个方法得到生存函数值。

```
# import hypsecant
from scipy.stats import hypsecant
beta = 1

# Using stats.hypsecant.sf() method
gfg = hypsecant.sf(0.3, beta)

print(gfg)
```

**输出:**

> 0.7065742294890258

**例 2 :**

```
# import hypsecant
from scipy.stats import hypsecant
beta = 4

# Using stats.hypsecant.sf() method
gfg = hypsecant.sf(0.9, beta)

print(gfg)
```

**输出:**

> 0.9713401642619637