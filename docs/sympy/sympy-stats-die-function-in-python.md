# Python 中的 sympy.stats.Die()函数

> 原文:[https://www . geesforgeks . org/sympy-stats-die-function-in-python/](https://www.geeksforgeeks.org/sympy-stats-die-function-in-python/)

借助`**sympy.stats.Die()**`方法，利用`sympy.stats.Die()`方法可以得到参数给定面数且参数本身定义有名称的平模。

> **语法:** `sympy.stats.Die(name, faces)`
> **返回:**返回一个有‘n’个面的公平骰子。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.stats.Die()`方法，我们能够使用该方法获得具有作为参数传递的‘n’个面的公平骰子。

```
# Import sympy and Die
from sympy.stats import Die, density

X = Die('X', 12)
# Using sympy.Die() method
gfg = density(X).dict

print(gfg)
```

**输出:**

> {1: 1/12, 2: 1/12, 3: 1/12, 4: 1/12, 5: 1/12, 6: 1/12, 7: 1/12, 8: 1/12, 9: 1/12, 10: 1/12, 11: 1/12, 12: 1/12}

**例 2 :**

```
# Import sympy and Die
from sympy.stats import Die, density

X = Die('X', 3)
# Using sympy.Die() method
gfg = density(X).dict

print(gfg)
```

**输出:**

> {1: 1/3, 2: 1/3, 3: 1/3}