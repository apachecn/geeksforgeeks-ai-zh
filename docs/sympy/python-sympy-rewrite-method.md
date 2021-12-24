# Python | sympy.rewrite()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-rewrite-method/](https://www.geeksforgeeks.org/python-sympy-rewrite-method/)

借助 **sympy.rewrite()** 方法，我们可以用另一个函数来表示任何数学函数。

> **语法:**表达式.重写(函数)
> 
> **参数:**
> **表达式–**是用另一个函数来表示的数学表达式。
> **函数–**它是用于重写给定表达式的数学函数。
> 
> **返回:**根据指定函数返回与输入对应的数学表达式。

**示例#1:**

```
# import sympy 
from sympy import * 

x = symbols('x')
expr = tan(x)
print("Expression = {}".format(expr))

# Use sympy.rewrite() method 
expr_in_terms_of_sin = expr.rewrite(sin)  

print("Expression in terms of sin() : {}".format(expr_in_terms_of_sin))  
```

**输出:**

```
Expression = tan(x)
Expression in terms of sin() : 2*sin(x)**2/sin(2*x)

```

**例 2:**

```
# import sympy 
from sympy import * 

x = symbols('x')
expr = factorial(x)
print("Expression = {}".format(expr))

# Use sympy.rewrite() method 
expr_in_terms_of_gamma = expr.rewrite(gamma)  

print("Expression in terms of gamma() : {}".format(expr_in_terms_of_gamma))  
```

**输出:**

```
Expression = factorial(x)
Expression in terms of gamma() : gamma(x + 1)

```