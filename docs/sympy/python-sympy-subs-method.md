# Python | sympy.subs()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-subs-method/](https://www.geeksforgeeks.org/python-sympy-subs-method/)

借助`**sympy.subs()**`方法，我们可以用`sympy.subs()`方法代入各种数学函数中的变量值。

> **语法:** `sympy.subs(source, destination)`
> **返回:**通过改变变量返回相同的表达式。

**示例#1 :**

在这个例子中我们可以看到，通过使用`sympy.subs()`方法，我们可以将现有变量的值替换为新变量。

```
# import sympy
from sympy import *

# symbol declaration
x, y = symbols('x y')

gfg_exp = cos(x) + 1

# use the method sympy.subs()
gfg_exp = gfg_exp.subs(x, y)

print(gfg_exp)
```

**输出:**

> cos(y) + 1

**例 2 :**

```
# import sympy
from sympy import *

# symbol declaration
x, y = symbols('x y')

gfg_exp = cos(x) + 1

# use the method sympy.subs()
gfg_exp = gfg_exp.subs(x, 0)

print(gfg_exp)
```

**输出:**

> Two