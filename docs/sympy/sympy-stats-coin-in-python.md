# Python 中的 sympy.stats.Coin()

> 原文:[https://www.geeksforgeeks.org/sympy-stats-coin-in-python/](https://www.geeksforgeeks.org/sympy-stats-coin-in-python/)

借助`**sympy.stats.Coin()**`方法，我们可以用`sympy.stats.Coin()`方法创造一个公平或不公平的硬币。一枚公平的硬币有一半**的概率**但是我们不能说是不公平的硬币。

> **语法:** `sympy.stats.Coin(name, value)`
> 
> **参数:**
> **名称–**它代表硬币的名称。
> **值–**默认情况下取一半，可以使用小于 1 的 Rational 值进行更改。
> 
> **返还:**返还公平或不公平的硬币。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.stats.Coin()`方法，我们能够使用该方法获得公平或不公平的硬币。

```py
# Import Sympy and Coin
from sympy.stats import Coin, density
from sympy import Rational

# Using sympy.Coin method
X = Coin('X')
gfg = density(X).dict

print(gfg)
```

**输出:**

```py
{H: 1/2, T: 1/2}

```

**例 2 :**

```py
# Import Sympy and Coin
from sympy.stats import Coin, density
from sympy import Rational

# Using sympy.Coin method
X = Coin('X', Rational(3, 5))
gfg = density(X).dict

print(gfg)
```

**输出:**

```py
{H: 3/5, T: 2/5}

```