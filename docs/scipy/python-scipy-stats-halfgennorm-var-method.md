# python \ scipy stat . halform . var()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-var-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-var-method/)

借助`**stats.halfgennorm.var()**`方法，我们可以利用`stats.halfgennorm.var()`方法得到分布的方差值。

> **语法:** `stats.halfgennorm.var(beta)`
> **返回:**返回分布的方差值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.halfgennorm.var()`方法，我们能够利用这个方法得到分布的方差值。

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 10

# Using stats.halfgennorm.var() method
gfg = halfgennorm.var(beta)

print(gfg)
```

**输出:**

> 0.08159018176509003

**例 2 :**

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.var() method
gfg = halfgennorm.var(beta)

print(gfg)
```

**输出:**

> 0.09899472128703718