# Python | sympy.is_constant()方法

> 原文:[https://www . geesforgeks . org/python-sympy-is _ constant-method/](https://www.geeksforgeeks.org/python-sympy-is_constant-method/)

借助`**sympy.is_constant()**`方法，我们可以检查元素是否恒定，如果发现恒定，它将使用`sympy.is_constant()`方法返回一个布尔值。

> **语法:** `sympy.is_constant()`
> **返回:**如果找到常量，返回布尔值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.is_constant()`方法，我们能够通过获取布尔值来检测常数。

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.is_constant() method
gfg = simplify(2).is_constant()

print(gfg)
```

**输出:**

> 真实的

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.is_constant() method
gfg = simplify(sin(x)).is_constant()

print(gfg)
```

**输出:**

> 错误的