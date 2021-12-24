# Python | sympy.powdenest()方法

> 原文:[https://www . geesforgeks . org/python-sympy-powden est-method/](https://www.geeksforgeeks.org/python-sympy-powdenest-method/)

借助`**sympy.powdenest()**`方法，我们可以利用恒等式简化数学表达式的幂，即`(x^a)^b=x^ab`。

> **语法:** `sympy.powdenest()`
> **返回:**返回使用恒等式的简化数学表达式。

**例#1 :**
在这个例子中，我们可以看到，通过使用`sympy.powdenest()`方法，我们能够利用恒等式简化数学表达式的幂，即`(x^a)^b=x^ab`。

```py
# import sympy
from sympy import * 

x, y = symbols('x y')
gfg_exp = (x**2)**3

# Use sympy.powdenest() method
fact = powdenest(gfg_exp)

print(fact)
```

**输出:**

> x**6

**例 2 :**

```py
# import sympy
from sympy import * 

x, y, z, a, b = symbols('x y z a b')
gfg_exp = (x**(a + b))**2

# Use sympy.powdenest() method
fact = powdenest(gfg_exp)

print(fact)
```

**输出:**

> x**(2*a + 2*b)