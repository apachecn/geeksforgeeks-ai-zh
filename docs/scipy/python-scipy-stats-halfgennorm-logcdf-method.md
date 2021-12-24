# Python | Scipy stats . half gennorm . logcdf()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-logcdf-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-logcdf-method/)

借助`**stats.halfgennorm.logcdf()**`方法，利用`stats.halfgennorm.logcdf()`方法可以得到累积分布函数的对数值。

> **语法:** `stats.halfgennorm.logcdf(x, beta)`
> **返回:**返回累计分布函数的对数值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`stats.halfgennorm.logcdf()`方法，我们能够使用该方法获得累积分布函数的对数值。

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1

# Using stats.halfgennorm.logcdf() method
gfg = halfgennorm.logcdf(0.3, beta)

print(gfg)
```

**输出:**

> -1.3502256128148469

**例 2 :**

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.logcdf() method
gfg = halfgennorm.logcdf(0.9, beta)

print(gfg)
```

**输出:**

> -0.12420246359133956