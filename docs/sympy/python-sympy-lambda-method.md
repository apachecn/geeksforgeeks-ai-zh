# Python | sympy。Lambda()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-lambda-method/](https://www.geeksforgeeks.org/python-sympy-lambda-method/)

借助`**sympy.Lambda()**`方法，我们只需定义公式就可以进行任何数学运算，然后使用`sympy.Lambda()`传递带有参考变量的参数。

> **语法:** `sympy.Lambda()`
> **返回:**返回数学公式的结果。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.Lambda()`方法，我们可以执行任何数学运算。

```py
# import sympy
from sympy import *

# Use sympy.Lambda() method
x = symbols('x')
gfg = Lambda(x, x + 1)

print(gfg(9))
```

**输出:**

> Ten

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.Lambda() method
x, y = symbols('x y')
gfg = Lambda((x, y), x * y)

print(gfg(9, 5))
```

**输出:**

> Forty-five