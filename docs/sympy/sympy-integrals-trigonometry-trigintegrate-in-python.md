# python 中的症状积分三角积分()

> 原文:[https://www . geeksforgeeks . org/sympy-integration-三角学-trigintegrate-in-python/](https://www.geeksforgeeks.org/sympy-integrals-trigonometry-trigintegrate-in-python/)

借助**trig integral()**方法，我们可以使用模式匹配计算三角函数的积分，并使用该方法返回积分函数。

> **语法:**trig integral(f，x，conds= '分片')
> 
> **返回:**返回综合功能

**示例#1 :**

在这个例子中我们可以看到，通过使用 **trigintegrate()** 方法，我们能够使用模式匹配获得三角函数的积分值。

## 蟒蛇 3

```
# import trigintegrate
from sympy import Symbol, sin, cos, tan, sec, csc, cot
from sympy.integrals.trigonometry import trigintegrate
from sympy.abc import x

# Using trigintegrate() method
gfg = trigintegrate(tan(x)/cos(x), x)

print(gfg)
```

**输出:**

> 1/cos(x)

**例 2 :**

## 蟒蛇 3

```
# import trigintegrate
from sympy import Symbol, sin, cos, tan, sec, csc, cot
from sympy.integrals.trigonometry import trigintegrate
from sympy.abc import x

# Using trigintegrate() method
gfg = trigintegrate(tan(x)*cot(x), x)

print(gfg)
```

**输出:**

> x