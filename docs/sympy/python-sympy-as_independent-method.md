# Python | sympy.as_independent()方法

> 原文:[https://www . geesforgeks . org/python-sympy-as _ independent-method/](https://www.geeksforgeeks.org/python-sympy-as_independent-method/)

借助`**sympy.as_independent()**`方法，我们可以通过在`sympy.as_independent()`方法中作为参数传递的变量来独立分离数学表达式。

> **语法:** `sympy.as_independent(variable)`
> 
> **Return :** 返回数学表达式中变量分离的元组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.as_independent()`方法，我们能够基于作为参数传递的自变量来分离数学函数。

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.as_independent(variable) method
gfg = (1 + 2 * x + 1 / x).as_independent(x)

print(gfg)
```

**输出:**

> (1，2*x + 1/x)

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.as_independent(variable) method
gfg = (1 / y**2 + x).as_independent(y)

print(gfg)
```

**输出:**

> (x，y**(-2))