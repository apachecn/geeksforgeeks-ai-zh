# Python | Scipy stats . hyp secant . fit()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-fit-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-fit-method/)

借助`**stats.hypsecant.fit()**`方法，我们可以利用`stats.hypsecant.fit()`方法得到一般数据的参数估计。

> **语法:** `stats.hypsecant.fit(data)`
> **返回:**返回通用数据的参数估计。

**示例#1 :**
在本例中，我们可以看到，通过使用`stats.hypsecant.fit()`方法，我们能够使用该方法获得通用数据的参数估计。

```py
# import hypsecant
from scipy.stats import hypsecant
data = [1, 2, 3, 4]

# Using stats.hypsecant.fit() method
gfg = hypsecant.fit(data)

print(gfg)
```

**输出:**

> (2.5000442723226115, 0.8418290927220122)

**例 2 :**

```py
# import hypsecant
from scipy.stats import hypsecant
data = [1, 2, 3, 4, 10, -5]

# Using stats.hypsecant.fit() method
gfg = hypsecant.fit(data)

print(gfg)
```

**输出:**

> (2.4999694801000487, 2.756410927671771)