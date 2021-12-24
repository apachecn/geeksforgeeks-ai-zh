# Python | sympy.is_number 方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ number-method/](https://www.geeksforgeeks.org/python-sympy-is_number-method/)

借助`**sympy.is_number**`方法，我们可以检查元素是否是数字，如果使用`sympy.is_number`方法找到数字，它将返回一个布尔值。

> **语法:** `sympy.is_number`
> **返回:**如果找到数字，返回布尔值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.is_number()`方法，我们能够通过获取布尔值来检测数字。

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.is_number method
gfg = cos(2).is_number

print(gfg)
```

**输出:**

> 真实的

**例 2 :**

```py
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.is_number method
gfg = sin(x).is_number

print(gfg)
```

**输出:**

> 错误的