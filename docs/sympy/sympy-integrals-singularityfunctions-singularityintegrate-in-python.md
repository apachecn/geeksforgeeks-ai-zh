# python 中的奇异积分.奇异函数.奇异积分()

> 原文:[https://www . geeksforgeeks . org/sympy-integration-singularity functions-singularity-integrate-in-python/](https://www.geeksforgeeks.org/sympy-integrals-singularityfunctions-singularityintegrate-in-python/)

借助**奇点积分()**方法，我们可以得到奇点函数的定积分，并利用这种方法返回积分函数。

> **语法:**奇点积分(f，x)
> 
> **返回:**返回函数的定积分。

**示例#1 :**

在这个例子中我们可以看到，通过使用**奇点积分()**方法，我们能够通过使用该方法得到奇点函数的定积分，并返回积分函数。

## 蟒蛇 3

```
# import singularityintegrate
from sympy.integrals.singularityfunctions import singularityintegrate
from sympy import SingularityFunction, symbols, Function

x, a, n, y = symbols('x a n y')
f = Function('f')

# Using singularityintegrate() method
gfg = singularityintegrate(SingularityFunction(x**2 + 1, a, 2), x)

print(gfg)
```

**输出:**

> 奇点函数(x**2 + 1，a，3)/3

**例 2 :**

## 蟒蛇 3

```
# import singularityintegrate
from sympy.integrals.singularityfunctions import singularityintegrate
from sympy import SingularityFunction, symbols, Function

x, a, n, y = symbols('x a n y')
f = Function('f')

# Using singularityintegrate() method
gfg = singularityintegrate(SingularityFunction(x**3, 4, -2), x)

print(gfg)
```

**输出:**

> 奇点函数(x**3，4，-1)