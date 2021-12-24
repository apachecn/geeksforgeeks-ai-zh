# python \ scipy stat . halform . RVs()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-RVs-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-rvs-method/)

借助于`**stats.halfgennorm.rvs()**`方法，我们可以利用`stats.halfgennorm.rvs()`方法从广义正态分布生成随机变量。

> **语法:** `stats.halfgennorm.rvs(beta)`
> **返回:**返回随机变量的值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.halfgennorm.rvs()`方法，我们能够用这个方法得到广义正态分布的随机变量。

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1

# Using stats.halfgennorm.rvs() method
gfg = halfgennorm.rvs(beta)

print(gfg)
```

**输出:**

> 1.2087830003416462

**例 2 :**

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.rvs() method
gfg = halfgennorm.rvs(beta)

print(gfg)
```

**输出:**

> 0.968700779140972