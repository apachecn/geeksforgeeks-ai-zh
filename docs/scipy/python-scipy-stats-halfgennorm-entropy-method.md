# Python | Scipy stats . half gennorm . entropy()方法

> 原文:[https://www . geesforgeks . org/python-scipy-stats-half gennorm-entropy-method/](https://www.geeksforgeeks.org/python-scipy-stats-halfgennorm-entropy-method/)

借助`**stats.halfgennorm.entropy()**`方法，我们可以利用`stats.halfgennorm.entropy()`方法得到随机变量的熵值。

> **语法:** `stats.halfgennorm.entropy(beta)`
> **返回:**返回随机变量的熵值。

**例#1 :**
在这个例子中我们可以看到，通过使用`stats.halfgennorm.entropy()`方法，我们能够通过使用这个方法得到随机变量的熵值。

```
# import halfgennorm
from scipy.stats import halfgennorm
beta = 2

# Using stats.halfgennorm.entropy() method
gfg = halfgennorm.entropy(beta)

print(gfg)
```

**输出:**

> 0.3792177623647547

**例 2 :**

```
# import halfgennorm
from scipy.stats import halfgennorm
beta = 4

# Using stats.halfgennorm.entropy() method
gfg = halfgennorm.entropy(beta)

print(gfg)
```

**输出:**

> 0.15172816357818686