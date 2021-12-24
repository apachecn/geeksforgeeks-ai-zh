# Python 中的 sympy.frac()方法

> 原文:[https://www.geeksforgeeks.org/sympy-frac-method-in-python/](https://www.geeksforgeeks.org/sympy-frac-method-in-python/)

**sympy.frac(x)** 函数表示 x 的小数部分，对于实数，定义为:**x –[ x]**

> **语法:** sympy.frac()
> 
> **返回:**返回简化的数学表达式。

**示例#1 :**

## 蟒蛇 3

```
# import sympy 
from sympy import *

# Use sympy.frac() method 
gfg = frac(5.36)

print(gfg)
```

**输出:**

```
0.36

```

**例 2 :**

## 蟒蛇 3

```
# import sympy 
from sympy import *

# Use sympy.frac() method 
gfg = frac(Rational(7, 5))

print(gfg)
```

**输出:**

```
2 / 5

```