# Python | sympy。函数()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-function-method/](https://www.geeksforgeeks.org/python-sympy-function-method/)

借助`**sympy.Function()**`方法，我们可以利用`sympy.Function()`方法找到整个数学表达式中的各种函数，如 f(x)、sin(x)、log(x)等。

> **语法:** `sympy.Function()`
> **返回:**返回数学运算中的函数列表。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.Function()`方法，我们能够在数学运算中找到函数。

```
# import sympy
from sympy import * 

x, y = symbols('x y')
f = Function('f')

# Use sympy.Function() method
gfg = (f(x) + 2 * tan(y + I * pi) + log(2 * x)).atoms(Function)

print(gfg)
```

**输出:**

> {f(x)，tan(y + I*pi)，log(2*x)}

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')
f = Function('f')

# Use sympy.Function() method
gfg = (2 + 3 * cos(y) + 5 * log(2 * x)).atoms(Function)

print(gfg)
```

**输出:**

> {cos(y)，log(2*x)}