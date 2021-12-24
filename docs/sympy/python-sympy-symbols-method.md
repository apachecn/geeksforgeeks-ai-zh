# Python | sympy.symbols()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-symbols-method/](https://www.geeksforgeeks.org/python-sympy-symbols-method/)

借助`**sympy.symbols()**`方法，我们可以用`sympy.symbols()`方法声明一些变量供数学表达式和多项式使用。

> **语法:** `sympy.symbols()`
> **返回:**不返回或不返回。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.symbols()`方法，我们能够获得数学表达式和多项式的变量。

```
# import sympy
from sympy import *

# Use sympy.symbols() method
x, y = symbols('x y')
x = 2
gfg = x**2 + 4 * x + 4

print(gfg)
```

**输出:**

> Sixteen

**例 2 :**

```
# import sympy
from sympy import *

# Use sympy.symbols() method
x, y = symbols('x y')
x = 5
y = 5
gfg = x**2 + y

print(gfg)
```

**输出:**

> Thirty