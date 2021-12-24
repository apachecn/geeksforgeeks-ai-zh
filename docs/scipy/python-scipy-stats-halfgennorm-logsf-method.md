# Python | Scipy stats . half gennorm . logsf()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-logsf-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-logsf-method/)

借助`**stats.halfgennorm.logsf()**`方法，利用`stats.halfgennorm.logsf()`方法可以得到生存函数的对数值，即**对数(1–CDF)**。

> **语法:** `stats.halfgennorm.logsf(x, beta)`
> **返回:**返回生存函数的日志值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`stats.halfgennorm.logsf()`方法，我们能够使用该方法获得生存函数的对数值。

```
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1

# Using stats.halfgennorm.logsf() method
gfg = halfgennorm.logsf(0.3, beta)

print(gfg)
```

**输出:**

> -0.2999999999999998

**例 2 :**

```
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.logsf() method
gfg = halfgennorm.logsf(0.9, beta)

print(gfg)
```

**输出:**

> -2.1473008279056534