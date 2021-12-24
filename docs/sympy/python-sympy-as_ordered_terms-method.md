# Python | sympy . as _ ordered _ terms()方法

> 原文:[https://www . geesforgeks . org/python-sympy-as _ ordered _ terms-method/](https://www.geeksforgeeks.org/python-sympy-as_ordered_terms-method/)

借助`**sympy.as_ordered_terms()**`方法，我们可以利用`sympy.as_ordered_terms()`方法得到变量排序的项。

> **语法:** `sympy.as_ordered_terms()`
> **返回:**返回数学表达式中的有序项。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.as_ordered_terms()`方法，我们能够得到数学表达式的项。

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.as_ordered_terms() method
gfg = (x**2 + 2 * x*y + y**2).as_ordered_terms()

print(gfg)
```

**输出:**

> [x**2，2*x*y，y**2]

**例 2 :**

```
# import sympy
from sympy import * 

x, y = symbols('x y')

# Use sympy.as_ordered_terms() method
gfg = (y + x).as_ordered_terms()

print(gfg)
```

**输出:**

> [x，y]