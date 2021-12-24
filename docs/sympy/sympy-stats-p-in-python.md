# 症状-统计。Python 中的 p()

> 原文:[https://www.geeksforgeeks.org/sympy-stats-p-in-python/](https://www.geeksforgeeks.org/sympy-stats-p-in-python/)

借助`**sympy.stats.P()**`方法，我们可以用`sympy.stats.P()`方法找到一个场合或一个假设情况的概率。

> **语法:** `sympy.stats.P(function)`
> **返回:**返回一个假设的概率。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.stats.P()`方法，我们能够使用该方法找到假设情况的概率。

```py
# Import sympy, P, Dice
from sympy.stats import P, Die

situation = Die('X', 2)

# Using stats.P() method
gfg = P(situation < 5)

print(gfg)
```

**输出:**

> one

**例 2 :**

```py
# Import sympy, P, Dice
from sympy.stats import P, Die

situation = Die('X', 6)

# Using stats.P() method
gfg = P(situation > 3)

print(gfg)
```

**输出:**

> 1/2