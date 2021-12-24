# Python | Scipy stats . half gennorm . STD()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-STD-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-std-method/)

借助`**stats.halfgennorm.std()**`方法，我们可以利用`stats.halfgennorm.std()`方法得到分布的标准差的值。

> **语法:** `stats.halfgennorm.std(beta)`
> **返回:**返回分布标准差的值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.halfgennorm.std()`方法，我们能够通过使用这个方法得到分布的标准差的值。

```
# import halfgennorm
from scipy.stats import halfgennorm
beta = 7

# Using stats.halfgennorm.std() method
gfg = halfgennorm.std(beta)

print(gfg)
```

**输出:**

> 0.29061475578761414

**例 2 :**

```
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.std() method
gfg = halfgennorm.std(beta)

print(gfg)
```

**输出:**

> 0.31463426591367505