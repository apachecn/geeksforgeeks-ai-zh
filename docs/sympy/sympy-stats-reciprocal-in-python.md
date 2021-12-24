# Python 中的 sympy.stats .倒数()

> 原文:[https://www . geesforgeks . org/sympy-stats-python 中的倒数/](https://www.geeksforgeeks.org/sympy-stats-reciprocal-in-python/)

借助`**sympy.stats.Reciprocal()**`方法，我们可以得到代表倒数分布的连续随机变量。

> **句法:** `sympy.stats.Reciprocal(name, a, b)`
> 其中，a 和 b 为实数，a、b >为 0。
> 
> **返回:**返回连续随机变量。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.stats.Reciprocal()`方法，我们能够使用该方法获得表示倒数分布的连续随机变量。

```py
# Import sympy and Reciprocal
from sympy.stats import Reciprocal, density
from sympy import Symbol, pprint

z = Symbol("z")
a = Symbol("a", positive = True)
b = Symbol("b", positive = True)

# Using sympy.stats.Reciprocal() method
X = Reciprocal("x", a, b)
gfg = density(X)(z)

print(gfg)
```

**输出:**

> 1/(x*(对数(a) +对数(b)))

**例 2 :**

```py
# Import sympy and Reciprocal
from sympy.stats import Reciprocal, density
from sympy import Symbol, pprint

z = 0.35
a = 1
b = 2

# Using sympy.stats.Reciprocal() method
X = Reciprocal("x", a, b)
gfg = density(X)(z)

print(gfg)
```

**输出:**

> 0.0861703622690834