# Python | Scipy stats . half gennorm .中位数()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-median-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-median-method/)

借助`**stats.halfgennorm.median()**`方法，我们可以利用`stats.halfgennorm.median()`方法得到分布的中值。

> **语法:** `stats.halfgennorm.median(beta)`
> **返回:**返回分布中值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.halfgennorm.median()`方法，我们能够利用这个方法得到分布的中值。

```
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1

# Using stats.halfgennorm.median() method
gfg = halfgennorm.median(beta)

print(gfg)
```

**输出:**

> 0.6931471805599455

**例 2 :**

```
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.median() method
gfg = halfgennorm.median(beta)

print(gfg)
```

**输出:**

> 0.4571463442259011