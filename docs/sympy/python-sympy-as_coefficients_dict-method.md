# Python | sympy . as _ coefficients _ dict()方法

> 原文:[https://www . geesforgeks . org/python-sympy-as _ coefficients _ dict-method/](https://www.geeksforgeeks.org/python-sympy-as_coefficients_dict-method/)

借助`**sympy.as_coefficients_dict()**`方法，我们能够通过使用`sympy.as_coefficients_dict()`方法找到存在于数学表达式中的字典中所有元素的系数。

> **语法:** `sympy.as_coefficients_dict()`
> **返回:**返回字典中数学表达式的系数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.as_coefficients_dict()`方法，我们可以找到一个数学表达式中的所有系数，并返回它的字典。

```
# import sympy
from sympy import * 

x = symbols('x')

# Use sympy.as_coefficients_dict() method
gfg = x**3 + 21 * x + 12

print(gfg.as_coefficients_dict())
```

**输出:**

> defaultdict(，{1: 12，x**3: 1，x: 21})

**例 2 :**

```
# import sympy
from sympy import * 

x = symbols('x')

# Use sympy.as_coefficients_dict() method
gfg = x**3 + 21 * x**2 + 121 * x + 4

print(gfg.as_coefficients_dict())
```

**输出:**

> defaultdict(，{1: 4，x**3: 1，x**2: 21，x: 121})