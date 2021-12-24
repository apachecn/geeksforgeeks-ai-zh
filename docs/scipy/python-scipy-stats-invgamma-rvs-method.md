# Python | Scipy stats . invgamma . RVs()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-invgamma-RVs-method/](https://www.geeksforgeeks.org/python-scipy-stats-invgamma-rvs-method/)

借助于`**stats.invgamma.rvs()**`方法，我们可以利用`stats.invgamma.rvs()`方法由反伽玛广义正态分布函数生成随机变量。

> **语法:** `stats.invgamma.rvs(a)`
> **返回:**返回随机变量的值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.invgamma.rvs()`方法，我们能够利用这个方法得到倒伽马广义正态分布的随机变量。

```py
# import invgamma
from scipy.stats import invgamma
a = 1

# Using stats.invgamma.rvs() method
gfg = invgamma.rvs(a)

print(gfg)
```

**输出:**

> 1.8920923678338413

**例 2 :**

```py
# import invgamma
from scipy.stats import invgamma
a = 4

# Using stats.invgamma.rvs() method
gfg = invgamma.rvs(a)

print(gfg)
```

**输出:**

> 0.3174183513521846