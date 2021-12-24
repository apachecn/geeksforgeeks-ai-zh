# Python | sympy.combsimp()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-combsimp-method/](https://www.geeksforgeeks.org/python-sympy-combsimp-method/)

借助 **sympy.combsimp()** 方法，我们可以简化组合表达式。

> **语法:** combsimp(表达式)
> 
> **参数:**
> **表达式–**是需要简化的组合表达式。
> 
> **返回:**返回与输入对应的简化数学表达式。

**示例#1:**

```
# import sympy 
from sympy import * 

n = symbols('n', integer = True)
expr = factorial(n)/factorial(n - 3)
print("Expression = {}".format(expr))

# Use sympy.combsimp() method 
simple_expr = combsimp(expr)  

print("Simplified Expression : {}".format(simple_expr))  
```

**输出:**

```
Expression = factorial(n)/factorial(n - 3)
Simplified Expression : n*(n - 2)*(n - 1)

```

**例 2:**

```
# import sympy 
from sympy import * 

n, k = symbols('n k', integer = True)
expr = binomial(n + 1, k + 1)/binomial(n, k)
print("Expression = {}".format(expr))

# Use sympy.combsimp() method 
simple_expr = combsimp(expr)  

print("Simplified Expression : {}".format(simple_expr))  
```

**输出:**

```
Expression = binomial(n+1, k+1)/binomial(n, k)
Simplified Expression : (n + 1)/(k + 1)

```