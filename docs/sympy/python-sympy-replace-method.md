# Python | sympy.replace()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-replace-method/](https://www.geeksforgeeks.org/python-sympy-replace-method/)

借助`**sympy.replace()**`方法，我们可以用`sympy.replace()`方法替换数学表达式中的函数，而无需编辑整个表达式。

> **语法:** `sympy.replace()`
> **返回:**返回数学表达式中被替换的值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.replace()`方法，我们能够替换表达式中的数学函数并返回更新后的表达式。

```
# import sympy
from sympy import * 

x, y = symbols('x y')

f = sin(x) + cos(2 * x)

# Use sympy.replace() method
gfg = f.replace(cos, sin)

print(gfg)
```

**输出:**

> sin(x) + sin(2*x)

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')

f = log(sin(x)) + tan(cos(2 * x))
# Use sympy.replace() method
gfg = f.replace(log, tan)

print(gfg)
```

**输出:**

> tan(sin(x)) + tan(cos(2*x))