# Python | Scipy stats . half gennorm . ISF()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-ISF-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-isf-method/)

借助`**stats.halfgennorm.isf()**`方法，我们可以利用`stats.halfgennorm.isf()`方法得到生存反函数的值，即**逆(1–CDF)**。

> **语法:** `stats.halfgennorm.isf(x, beta)`
> **返回:**返回逆生存函数的值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.halfgennorm.isf()`方法，我们能够通过使用这个方法得到逆生存函数值。

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1

# Using stats.halfgennorm.isf() method
gfg = halfgennorm.isf(0.3, beta)

print(gfg)
```

**输出:**

> 1.2039728043259357

**例 2 :**

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.isf() method
gfg = halfgennorm.isf(0.9, beta)

print(gfg)
```

**输出:**

> 0.09064147135377666