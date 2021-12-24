# Python | Scipy stats . half gennorm . pdf()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-pdf-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-pdf-method/)

借助`**stats.halfgennorm.pdf()**`方法，我们可以利用`stats.halfgennorm.pdf()`方法得到概率密度函数值。

半根范数的概率密度函数是
![](img/6c3e28301a788e0bb8dde099720345fc.png)

> **语法:** `stats.halfgennorm.pdf(x, beta)`
> **返回:**返回概率密度函数值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`stats.halfgennorm.pdf()`方法，我们能够使用该方法获得概率密度函数的值。

```
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1

# Using stats.halfgennorm.pdf() method
gfg = halfgennorm.pdf(0.3, beta)

print(gfg)
```

**输出:**

> 0.7408182206817179

**例 2 :**

```
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.pdf() method
gfg = halfgennorm.pdf(0.9, beta)

print(gfg)
```

**输出:**

> 0.5724509846343838