# Python | Scipy stats . half gennorm . PPF()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-PPF-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-ppf-method/)

借助`**stats.halfgennorm.ppf()**`方法，我们可以利用`stats.halfgennorm.ppf()`方法得到百分点函数的值，即**逆(cdf )** 。

> **语法:** `stats.halfgennorm.ppf(x, beta)`
> **返回:**返回百分点函数的值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`stats.halfgennorm.ppf()`方法，我们能够使用该方法获得百分点函数的值。

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1

# Using stats.halfgennorm.ppf() method
gfg = halfgennorm.ppf(0.3, beta)

print(gfg)
```

**输出:**

> 0.3566749439387324

**例 2 :**

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.ppf() method
gfg = halfgennorm.ppf(0.9, beta)

print(gfg)
```

**输出:**

> 0.9307267047740223