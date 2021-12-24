# Python | sympy.factor()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-factor-method/](https://www.geeksforgeeks.org/python-sympy-factor-method/)

借助`**sympy.factor()**`方法，我们可以利用`sympy.factor()`方法找到变量形式的数学表达式的因子。

> **语法:** `sympy.factor(expression)`
> **返回:**数学表达式的返回因子。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.factor()`方法，我们可以找到数学表达式中带有变量的因子。这里我们也使用`symbols()`方法将变量声明为符号。

```
# import sympy
from sympy import expand, symbols, factor

x, y = symbols('x y')
gfg_exp = x + y
exp = sympy.expand(gfg_exp**2)

# Use sympy.factor() method
fact = factor(exp)

print(fact)
```

**输出:**

> (x + y)**2

**例 2 :**

```
# import sympy
from sympy import expand, symbols, factor

x, y, z = symbols('x y z')
gfg_exp = x + y + z
exp = sympy.expand(gfg_exp**2)

# Use sympy.factor() method
fact = factor(exp)

print(fact)
```

**输出:**

> (x + y + z)**2