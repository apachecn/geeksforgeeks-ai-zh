# Python | Scipy stats . hyp secant . logsf()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-logsf-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-logsf-method/)

借助`**stats.hypsecant.logsf()**`方法，利用`stats.hypsecant.logsf()`方法可以得到生存函数的对数值，即**对数(1–CDF)**。

> **语法:** `stats.hypsecant.logsf(x, beta)`
> **返回:**返回生存函数的日志值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`stats.hypsecant.logsf()`方法，我们能够使用该方法获得生存函数的对数值。

```
# import hypsecant
from scipy.stats import hypsecant
beta = 1

# Using stats.hypsecant.logsf() method
gfg = hypsecant.logsf(0.3, beta)

print(gfg)
```

**输出:**

> -0.3473270158670634

**例 2 :**

```
# import hypsecant
from scipy.stats import hypsecant
beta = 4

# Using stats.hypsecant.logsf() method
gfg = hypsecant.logsf(0.9, beta)

print(gfg)
```

**输出:**

> -0.029078548392065258