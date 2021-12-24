# Python | sympy.has()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-has-method/](https://www.geeksforgeeks.org/python-sympy-has-method/)

借助`**sympy.has()**`方法，我们可以检查该数学表达式中是否使用了变量，这将通过使用`sympy.has()`方法返回一个布尔值。

> **语法:** `sympy.has(variable)`
> **返回:**返回布尔值，即真或假。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.has()`方法，我们能够检查变量是否用于数学表达式中。

```py
# import sympy
from sympy import * 

x, y, z = symbols('x y z')

# Use sympy.has() method
gfg = (3 * x + 2 * tan(y + I * pi) + log(2 * x)).has(x)

print(gfg)
```

**输出:**

> 真实的

**例 2 :**

```py
# import sympy
from sympy import * 

x, y, z = symbols('x y z')

# Use sympy.has() method
gfg = (3 * sin(x) + 2 * tan(y + I * pi)).has(z)

print(gfg)
```

**输出:**

> 错误的