# Python 中的 sympy.stats.FiniteRV()函数

> 原文:[https://www . geesforgeks . org/sympy-stats-finiterv-function-in-python/](https://www.geeksforgeeks.org/sympy-stats-finiterv-function-in-python/)

借助`**sympy.stats.FiniteRV()**`方法，我们可以通过使用`sympy.stats.FiniteRV()`方法创建一个给出密度字典的随机变量。

> **语法:** `sympy.stats.FiniteRV(name, dict)`
> 
> **返回:**返回具有密度字典的变量。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.stats.FiniteRV()`方法，我们能够使用该方法创建表示密度字典的随机变量。

```py
# Import sympy and FiniteRV
from sympy.stats import FiniteRV, P, E

# Using sympy.stats.FiniteRV() method
density = {0: .1, 1: .2, 2: .3, 3: .4}
X = FiniteRV('X', density)
print(E(X))

gfg = P(X > 2)
print(gfg)
```

**输出:**

```py
2.00000000000000
0.40000000000000

```

**例 2 :**

```py
# Import sympy and FiniteRV
from sympy.stats import FiniteRV, P, E

# Using sympy.stats.FiniteRV() method
density = {0: .11, 1: .20, 2: .13, 3: .4, 4: 0.16}
X = FiniteRV('X', density)
print(E(X))

gfg = P(X >= 3)
print(gfg)
```

**输出:**

```py
2.30000000000000
0.56000000000000

```