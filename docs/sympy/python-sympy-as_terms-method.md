# Python | sympy.as_terms()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-as_terms-method/](https://www.geeksforgeeks.org/python-sympy-as_terms-method/)

借助`**sympy.as_terms()**`方法，我们可以利用`sympy.as_terms()`方法得到作为一个项列表的数学表达式。

> **语法:** `sympy.as_terms()`
> **返回:**返回数学表达式中的术语列表。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.as_terms()`方法，我们能够获得列表中数学表达式的项。

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.as_terms() method
gfg = (x**2 + 2 * x*y + y**2).as_terms()

print(gfg)
```

**输出:**

> ([(x**2，((1.0，0.0)，(2，0)，()))，(y**2，((1.0，0.0)，(0，2)，()))，(2*x*y，((2.0，0.0)，(1，1)，())))]，[x，y])

**例 2 :**

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.as_terms() method
gfg = (y + x).as_terms()

print(gfg)
```

**输出:**

> ([(x，((1.0，0.0)，(1，0)，()))，(y，((1.0，0.0)，(0，1)，())))]，[x，y])