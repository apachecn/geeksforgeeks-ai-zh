# Python | Scipy stats . hyp secant . pdf()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-hyp secant-pdf-method/](https://www.geeksforgeeks.org/python-scipy-stats-hypsecant-pdf-method/)

借助`**stats.hypsecant.pdf()**`方法，我们可以利用`stats.hypsecant.pdf()`方法得到概率密度函数值。

超正割的概率密度函数为
![](img/df80d232daae528014db0427a9d30026.png)

> **语法:** `stats.hypsecant.pdf(x, beta)`
> **返回:**返回概率密度函数值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`stats.hypsecant.pdf()`方法，我们能够使用该方法获得概率密度函数的值。

```py
# import hypsecant
from scipy.stats import hypsecant
beta = 1

# Using stats.hypsecant.pdf() method
gfg = hypsecant.pdf(0.3, beta)

print(gfg)
```

**输出:**

> 0.25359922429233667

**例 2 :**

```py
# import hypsecant
from scipy.stats import hypsecant
beta = 4

# Using stats.hypsecant.pdf() method
gfg = hypsecant.pdf(0.9, beta)

print(gfg)
```

**输出:**

> 0.028621128378351488