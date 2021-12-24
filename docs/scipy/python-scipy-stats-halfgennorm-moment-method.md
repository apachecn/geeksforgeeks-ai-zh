# Python | Scipy stats . half gennorm . moment()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-moment-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-moment-method/)

借助`**stats.halfgennorm.moment()**`方法，利用`stats.halfgennorm.moment()`方法可以得到 n 阶非中心矩的值。

> **语法:** `stats.halfgennorm.moment(n, beta)`
> **返回:**返回非中心时刻的值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.halfgennorm.moment()`方法，我们能够通过使用这个方法得到非中心矩的值。

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1

# Using stats.halfgennorm.moment() method
gfg = halfgennorm.moment(3, beta)

print(gfg)
```

**输出:**

> 5.999999999999632

**例 2 :**

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.moment() method
gfg = halfgennorm.moment(4, beta)

print(gfg)
```

**输出:**

> 0.25000000001141554