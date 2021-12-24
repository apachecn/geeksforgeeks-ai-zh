# python 中的 sympy . integrates . delta functions . delta integrate()

> 原文:[https://www . geeksforgeeks . org/sympy-integrations-delta functions-delta integrate-in-python/](https://www.geeksforgeeks.org/sympy-integrals-deltafunctions-deltaintegrate-in-python/)

借助 **deltaintegrate()** 方法，我们可以计算 delta 函数的积分，并使用该方法返回积分函数。此方法使用增量表达式来执行集成。

> **语法:**deltaintegral(f，x)
> 
> **返回:**返回综合功能。

**示例#1 :**

在这个例子中，我们可以看到通过使用 **deltaintegrate()** 方法，我们能够通过使用这个方法得到 delta 函数的积分，并且它将返回积分的 delta 表达式。

## 蟒蛇 3

```
# import deltaintegrate
from sympy.abc import x, y, z
from sympy.integrals.deltafunctions import deltaintegrate
from sympy import sin, cos, tan, DiracDelta, Heaviside

# Using deltaintegrate() method
gfg = deltaintegrate(tan(x)*sin(x)*cos(x)*DiracDelta(x**2 - 1), x)

print(gfg)
```

**输出:**

> sin(1)* cos(1)* tan(1)* Hewiside(x–1)/2+sin(1)* cos(1)* tan(1)* Hewiside(x+1)/2

**例 2 :**

## 蟒蛇 3

```
# import deltaintegrate
from sympy.abc import x, y, z
from sympy.integrals.deltafunctions import deltaintegrate
from sympy import sin, cos, DiracDelta, Heaviside

# Using deltaintegrate() method
gfg = deltaintegrate(sin(y)*DiracDelta(x - z)*DiracDelta(y - z), y)

print(gfg)
```

**输出:**

> sin(z)* DiracDelta(x–z)* Hewiside(y–z)