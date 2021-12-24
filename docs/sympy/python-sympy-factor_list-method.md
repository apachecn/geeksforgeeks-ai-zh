# Python | sympy.factor_list()方法

> 原文:[https://www . geesforgeks . org/python-sympy-factor _ list-method/](https://www.geeksforgeeks.org/python-sympy-factor_list-method/)

借助 **sympy.factor_list()** 方法，我们可以在 *SymPy* 中以*(因子，幂)*元组的形式得到一个数学表达式的因子列表。

> **语法:** factor_list(表达式)
> 
> **参数:**
> **表达式**——它是一个数学表达式。
> 
> **返回:**以*(因子，幂)*元组的形式返回给定数学表达式的因子列表。

**示例#1:**
在这个示例中，我们可以看到，通过使用 **sympy.factor_list()** 方法，我们可以获得给定数学表达式的因子列表。

```
# import sympy
from sympy import * x = symbols('x')
expr = x**2 * z + 4 * x*y * z + 4 * y**2 * z

print("Mathematical expression : {}".format(expr))

# Use sympy.factor_list() method
f = factor_list(expr) 

print("List of factors : {}".format(f)) 
```

**输出:**

```
Mathematical expression : x**2*z + 4*x*y*z + 4*y**2*z
List of factors : (1, [(z, 1), (x + 2*y, 2)])

```

**例 2:**

```
# import sympy
from sympy import * x = symbols('x')
expr = (x**2 - 2 * x + 1)

print("Mathematical expression : {}".format(expr))

# Use sympy.factor_list() method
f = factor_list(expr) 

print("List of factors : {}".format(f)) 
```

**输出:**

```
Mathematical expression : x**2 - 2*x + 1
List of factors : (1, [(x - 1, 2)])

```