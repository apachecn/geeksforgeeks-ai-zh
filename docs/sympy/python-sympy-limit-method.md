# Python | sympy.limit()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-limit-method/](https://www.geeksforgeeks.org/python-sympy-limit-method/)

借助 **sympy.limit()** 方法，我们可以找到任何数学表达式的极限，
例如，

(1) ![\begin{equation*} \lim_{x\to a} f(x) \end{equation*}  ](img/5ccfd99c93e1c5836c90756c49317941.png "Rendered by QuickLaTeX.com")

> **语法:**极限(表达式、变量、值)
> **参数:**
> **表达式–**要对其执行极限运算的数学表达式，即 f(x)。
> **变量–**是数学表达式中的变量，即 x
> **值–**是极限趋于的值，即 a.
> **返回:**返回给定条件下数学表达式的极限。

**示例#1:**

## 蟒蛇 3

```
# import sympy
from sympy import *

x = symbols('x')
expr = sin(x)/x;

print("Expression : {}".format(expr))

# Use sympy.limit() method
limit_expr = limit(expr, x, 0) 

print("Limit of the expression tends to 0 : {}".format(limit_expr)) 
```

**输出:**

```
Expression : sin(x)/x
Limit of the expression tends to 0 : 1
```

**例 2:**

## 蟒蛇 3

```
# import sympy
from sympy import *

x = symbols('x')
expr = sin(3 * x)/x;

print("Expression : {}".format(expr))

# Use sympy.limit() method
limit_expr = limit(expr, x, 0) 

print("Limit of the expression tends to 0 : {}".format(limit_expr)) 
```

**输出:**

```
Expression : sin(3*x)/x
Limit of the expression tends to 0 : 3
```