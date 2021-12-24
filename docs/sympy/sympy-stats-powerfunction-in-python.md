# Python 中的 sympy.stats.PowerFunction()

> 原文:[https://www . geesforgeks . org/sympy-stats-power function-in-python/](https://www.geeksforgeeks.org/sympy-stats-powerfunction-in-python/)

借助`**sympy.stats.PowerFunction()**`方法，我们可以得到代表幂函数分布的连续随机变量。

![](img/6fc3ac3b15411a9369b929512b2efe4e.png)

> **语法:** `sympy.stats.PowerFunction(name, alpha, a, b)`
> 其中，a、b、alpha 为实数。
> 
> **返回:**返回连续随机变量。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.stats.PowerFunction()`方法，我们能够使用该方法获得表示幂函数分布的连续随机变量。

```py
# Import sympy and PowerFunction
from sympy.stats import PowerFunction, density
from sympy import Symbol, pprint

z = Symbol("z")
alpha = Symbol("alpha", positive = True)
a = Symbol("a", positive = True)
b = Symbol("b", positive = True)

# Using sympy.stats.PowerFunction() method
X = PowerFunction("x", alpha, a, b)
gfg = density(X)(z)

print(gfg)
```

**输出:**

> (-2*a + 2*z)/(-a + b)**2

**例 2 :**

```py
# Import sympy and PowerFunction
from sympy.stats import PowerFunction, density, variance
from sympy import Symbol, pprint

z = Symbol("z")
alpha = 2
a = 0
b = 1

# Using sympy.stats.PowerFunction() method
X = PowerFunction("x", alpha, a, b)
gfg = density(X)(z)

pprint(variance(gfg))
```

**输出:**

> 1/18