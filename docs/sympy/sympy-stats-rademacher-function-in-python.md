# Python 中的 sympy.stats.Rademacher()函数

> 原文:[https://www . geesforgeks . org/sympy-stats-rademacher-function-in-python/](https://www.geeksforgeeks.org/sympy-stats-rademacher-function-in-python/)

**拉德马赫分布**是随机变量一半概率为+1，一半概率为-1 时的离散概率分布。借助`**sympy.stats.Rademacher()**`方法，我们可以用`sympy.stats.Rademacher()`方法创建具有随机分布的随机变量。

> **语法:** `sympy.stats.Rademacher(name)`
> 
> **返回:**返回拉德马赫分布。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.stats.Rademacher()`方法，我们能够使用该方法获得拉德马赫分布的随机变量。

```
# Import sympy and Rademacher
from sympy.stats import Rademacher, density

# Using sympy.stats.Rademacher() method
X = Rademacher('X')
gfg = density(X).dict

print(gfg)
```

**输出:**

```
{1: 1/2, -1: 1/2}

```

**例 2 :**

```
# Import sympy and Rademacher
from sympy.stats import Rademacher, density, P

# Using sympy.stats.Rademacher() method
X = Rademacher('X')
gfg = density(X).dict

print(P(gfg >= 0))
```

**输出:**

```
1/2

```