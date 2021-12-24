# Python 中的 sympy.stats.Geometric()

> 原文:[https://www . geesforgeks . org/sympy-stats-geometric-in-python/](https://www.geeksforgeeks.org/sympy-stats-geometric-in-python/)

借助`**sympy.stats.Geometric()**`方法，我们可以得到一个表示几何分布的随机变量。

> **语法:** `sympy.stats.Geometric(name, P)`
> 其中，P 代表概率
> **返回:**返回几何分布的随机变量。

**例#1 :**
在这个例子中我们可以看到，通过使用`sympy.stats.Geometric()`方法，我们能够通过使用这个方法得到表示几何分布的随机变量。

```
# Import sympy and geometric
from sympy.stats import Geometric, density, E, variance
from sympy import Symbol, S

p = S.One / 5

# Using sympy.stats.Geometric() method
X = Geometric("x", p)
gfg = density(X)(z)

print(variance(X))
```

**输出:**

> Twenty

**例 2 :**

```
# Import sympy and geometric
from sympy.stats import Geometric, density, E, variance
from sympy import Symbol, S

# Using sympy.stats.Geometric() method
X = Geometric("x", 0.4)
gfg = density(X)(z)

print(variance(X))
```

**输出:**

> 3.75000000000000