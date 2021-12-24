# Python | sympy . is _ 多项式()方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ 多项式-method/](https://www.geeksforgeeks.org/python-sympy-is_polynomial-method/)

借助`**sympy.is_polynomial()**`方法，我们可以通过`sympy.is_polynomial()`方法检查如果找到多项式，它将作为布尔值返回真。

> **语法:** `sympy.is_polynomial()`
> **返回:**如果找到多项式，返回布尔值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.is_polynomial()`方法，我们能够通过获取布尔值来检测多项式。

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.is_polynomial() method
gfg = simplify(x**2 + 2 * y*x + y**2).is_polynomial()

print(gfg)
```

**输出:**

> 真实的

**例 2 :**

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.is_constant() method
gfg = simplify(sin(x)).is_constant()

print(gfg)
```

**输出:**

> 错误的