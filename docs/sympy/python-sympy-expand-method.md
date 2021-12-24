# Python | sympy.expand()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-expand-method/](https://www.geeksforgeeks.org/python-sympy-expand-method/)

借助`**sympy.expand()**`方法，我们可以利用`sympy.expand()`方法将数学表达式展开为变量的形式。

> **语法:** `sympy.expand(expression)`
> **返回:**返回数学表达式。

**例#1 :**
在这个例子中我们可以看到，通过使用`sympy.expand()`方法，我们可以得到带有变量的数学表达式。这里我们也使用`symbols()`方法将变量声明为符号。

```
# import sympy
from sympy import expand, symbols

x, y = symbols('x y')
gfg_exp = x + y

# Use sympy.expand() method
exp = sympy.expand(gfg_exp**2)

print(exp)
```

**输出:**

> x**2 + 2*x*y + y**2

**例 2 :**

```
# import sympy
from sympy import expand, symbols

x, y, z = symbols('x y z')
gfg_exp = x + y + z

# Use sympy.expand() method
exp = sympy.expand(gfg_exp**2)

print(exp)
```

**输出:**

> x * * 2+2 * x * y+2 * x * z+y * * 2+2 * y * z+z * * 2