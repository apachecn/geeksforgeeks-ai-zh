# Python | sympy.atoms()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-atoms-method/](https://www.geeksforgeeks.org/python-sympy-atoms-method/)

借助`**sympy.atoms()**`方法，我们可以通过使用`sympy.atoms()`提取数学函数的原子值，如任何数字、符号等。

> **语法:** `sympy.atoms()`
> **返回:**从数学表达式中返回原子值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.atoms()`方法，我们可以通过任何数学运算获得原子值。

```py
# import sympy
from sympy import *

# Use sympy.atoms() method
x = symbols('x')
gfg = (2 + x + 7 * tan(x + I * pi)).atoms(Number)

print(gfg)
```

**输出:**

> {2, 7}

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.atoms() method
x = symbols('x')
gfg = (2 + x + 7 * log(x + I * pi)).atoms(Number, Symbol, NumberSymbol)

print(gfg)
```

**输出:**

> {pi，2，x，7}