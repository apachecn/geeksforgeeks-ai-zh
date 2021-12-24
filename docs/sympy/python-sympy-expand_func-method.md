# Python | sympy.expand_func()方法

> 原文:[https://www . geesforgeks . org/python-sympy-expand _ func-method/](https://www.geeksforgeeks.org/python-sympy-expand_func-method/)

借助 **sympy.expand_func()** 方法，我们可以用一些数学恒等式展开特殊函数。

> **语法:** expand_func(表达式)
> 
> **参数:**
> **表达式–**是要展开的数学表达式。
> 
> **返回:**根据一些数学恒等式返回与输入对应的数学表达式。

**示例#1:**

```
# import sympy 
from sympy import * 

x = symbols('x')
expr = gamma(x + 3)
print("Expression = {}".format(expr))

# Use sympy.expand_func() method 
expand_expr = expand_func(expr)  

print("Expanded Expression : {}".format(expand_expr))  
```

**输出:**

```
Expression = gamma(x + 3)
Expanded Expression : x*(x + 1)*(x + 2)*gamma(x)

```

**例 2:**

```
# import sympy 
from sympy import * 

x = symbols('x')
expr = binomial(x, 3)
print("Expression = {}".format(expr))

# Use sympy.expand_func() method 
expand_expr = expand_func(expr)  

print("Expanded Expression : {}".format(expand_expr))  
```

**输出:**

```
Expression = binomial(x, 3)
Expanded Expression : x*(x - 2)*(x - 1)/6

```