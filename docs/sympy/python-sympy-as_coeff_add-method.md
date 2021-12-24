# Python | sympy.as_coeff_add()方法

> 原文:[https://www . geesforgeks . org/python-sympy-as _ coeff _ add-method/](https://www.geeksforgeeks.org/python-sympy-as_coeff_add-method/)

借助`**sympy.as_coeff_add()**`方法，我们可以通过 **+** 符号分离数学表达式，并通过`sympy.as_coeff_add()`方法返回一个元组。

> **语法:** `sympy.as_coeff_add()`
> **返回:**返回由 **+** 符号分隔的元素元组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.as_coeff_add()`方法，我们能够获得由 **+** 符号分隔的元素元组。

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Using sympy.as_coeff_add() method
gfg = (x + 2 * y).as_coeff_add()

print(gfg)
```

**输出:**

> (0，(x，2*y))

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Using sympy.as_coeff_add() method
gfg = (x**2 + 4 * x + 4).as_coeff_add()

print(gfg)
```

**输出:**

> (4，(x**2，4*x))