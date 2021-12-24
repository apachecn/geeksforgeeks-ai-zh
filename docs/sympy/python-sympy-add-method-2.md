# Python | sympy。添加()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-add-method-2/](https://www.geeksforgeeks.org/python-sympy-add-method-2/)

借助`**sympy.Add()**`方法，我们可以将两个变量相加，利用`sympy.Add()`方法可以形成一个数学表达式。

> **语法:** `sympy.Add()`
> **返回:**返回两个变量的相加。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.Add()`方法，我们能够将变量的数量相加，并且可以形成数学表达式。

```
# import sympy
from sympy import * 

x = symbols('x')

# Use sympy.Add() method
gfg = Add(x, x)

print(gfg)
```

**输出:**

> 2*x

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.Add() method
gfg = Add(x, y)

print(gfg)
```

**输出:**

> x + y