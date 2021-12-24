# Python | Scipy stats . half gennorm . mean()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-mean-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-mean-method/)

借助`**stats.halfgennorm.mean()**`方法，我们可以用`stats.halfgennorm.mean()`方法得到分布的平均值。

> **语法:** `stats.halfgennorm.mean(beta)`
> **返回:**返回分布均值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.halfgennorm.mean()`方法，我们能够通过使用这个方法得到分布的平均值。

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1

# Using stats.halfgennorm.mean() method
gfg = halfgennorm.mean(beta)

print(gfg)
```

**输出:**

> 0.9999999999999998

**例 2 :**

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.mean() method
gfg = halfgennorm.mean(beta)

print(gfg)
```

**输出:**

> 0.4888705337199305