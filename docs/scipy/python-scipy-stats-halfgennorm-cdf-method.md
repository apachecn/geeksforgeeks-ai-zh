# Python | Scipy stats . half gennorm . CDF()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-CDF-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-cdf-method/)

借助`**stats.halfgennorm.cdf()**`方法，我们可以利用`stats.halfgennorm.cdf()`方法得到累积分布函数值。

> **语法:** `stats.halfgennorm.cdf(x, beta)`
> **返回:**返回累计分布函数值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.halfgennorm.cdf()`方法，我们能够通过使用这个方法得到累积分布函数值。

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1

# Using stats.halfgennorm.cdf() method
gfg = halfgennorm.cdf(0.3, beta)

print(gfg)
```

**输出:**

> 0.25918177931828207

**例 2 :**

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.cdf() method
gfg = halfgennorm.cdf(0.9, beta)

print(gfg)
```

**输出:**

> 0.8832010067319619