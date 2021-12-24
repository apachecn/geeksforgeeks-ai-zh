# Python | Scipy stats . half gennorm . fit()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-fit-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-fit-method/)

借助`**stats.halfgennorm.fit()**`方法，我们可以利用`stats.halfgennorm.fit()`方法得到一般数据的参数估计。

> **语法:** `stats.halfgennorm.fit(data, beta)`
> **返回:**返回通用数据的参数估计。

**示例#1 :**
在本例中，我们可以看到，通过使用`stats.halfgennorm.fit()`方法，我们能够使用该方法获得通用数据的参数估计。

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 1
data = [1, 2, 3, 4]

# Using stats.halfgennorm.fit() method
gfg = halfgennorm.fit(data, beta)

print(gfg)
```

**输出:**

> (0.747842031646833, 0.999999999643278, 0.9104743888803231)

**例 2 :**

```py
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4
data = [1, 2, 3, 4]

# Using stats.halfgennorm.fit() method
gfg = halfgennorm.fit(data, beta)

print(gfg)
```

**输出:**

> (283.5624794926913, 0.9950868221655309, 3.0513233113282805)