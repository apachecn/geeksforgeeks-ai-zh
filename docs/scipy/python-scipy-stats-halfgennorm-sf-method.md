# Python | Scipy stats . half gennorm . SF()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-SF-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-sf-method/)

借助`**stats.halfgennorm.sf()**`方法，我们可以利用`stats.halfgennorm.sf()`方法得到生存函数值为**1–CDF**。

> **语法:** `stats.halfgennorm.sf(x, beta)`
> **返回:**返回生存函数的值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.halfgennorm.sf()`方法，我们能够通过使用这个方法得到生存函数值。

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1

# Using stats.halfgennorm.sf() method
gfg = halfgennorm.sf(0.3, beta)

print(gfg)
```

**输出:**

> 0.740818220681718

**例 2 :**

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.sf() method
gfg = halfgennorm.sf(0.9, beta)

print(gfg)
```

**输出:**

> 0.11679899326803797