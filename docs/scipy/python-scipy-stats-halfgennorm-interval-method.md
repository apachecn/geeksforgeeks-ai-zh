# Python | Scipy stats . half gennorm . interval()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-interval-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-interval-method/)

借助`**stats.halfgennorm.interval()**`方法，我们可以利用`stats.halfgennorm.interval()`方法得到包含分布α%的范围的端点值。

> **语法:** `stats.halfgennorm.interval(alpha, beta)`
> **返回:**返回分布端点的值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.halfgennorm.interval()`方法，我们能够通过使用这个方法得到分布的端点值。

```
# import halfgennorm
from scipy.stats import halfgennorm
alpha, beta = 0.1, 5

# Using stats.halfgennorm.interval() method
gfg = halfgennorm.interval(alpha, beta)

print(gfg)
```

**输出:**

> (0.4140124809044803, 0.5078251542451746)

**例 2 :**

```
# import halfgennorm
from scipy.stats import halfgennorm
alpha, beta = 0.1, 1

# Using stats.halfgennorm.interval() method
gfg = halfgennorm.interval(alpha, beta)

print(gfg)
```

**输出:**

> (0.5978370007556202, 0.7985076962177717)