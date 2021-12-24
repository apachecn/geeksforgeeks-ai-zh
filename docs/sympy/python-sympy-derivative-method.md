# Python | sympy。导数()方法

> 原文:[https://www . geesforgeks . org/python-sympy-微商-method/](https://www.geeksforgeeks.org/python-sympy-derivative-method/)

借助**症状。导数()**方法，我们可以创建一个未赋值的 SymPy 表达式的导数。其语法与 **[diff()](https://www.geeksforgeeks.org/python-sympy-diff-method/)** 方法相同。要评估未估值的衍生产品，请使用 **[doit()](https://www.geeksforgeeks.org/python-sympy-doit-method/)** 方法。

> **语法:**导数(表达式，引用变量)
> 
> **参数:**
> **表达式–**一个其未赋值导数被找到的符号表达式。
> **参考变量–**找到导数的变量。
> 
> **返回:**返回给定表达式的未赋值导数。

**示例#1:**

```py
# import sympy 
from sympy import * 

x, y = symbols('x y')
expr = x**2 + 2 * y + y**3
print("Expression : {} ".format(expr))

# Use sympy.Derivative() method 
expr_diff = Derivative(expr, x)  

print("Derivative of expression with respect to x : {}".format(expr_diff))  
print("Value of the derivative : {} ".format(expr_diff.doit()))
```

**输出:**

```py
Expression : x**2 + y**3 + 2*y 
Derivative of expression with respect to x : Derivative(x**2 + y**3 + 2*y, x)
Value of the derivative : 2*x 

```

**例 2:**

```py
# import sympy 
from sympy import * 

x, y = symbols('x y')
expr = y**2 * x**2 + 2 * y*x + x**3 * y**3
print("Expression : {} ".format(expr))

# Use sympy.Derivative() method 
expr_diff = Derivative(expr, x, y)  

print("Derivative of expression with respect to x : {}".format(expr_diff))  
print("Value of the derivative : {} ".format(expr_diff.doit()))
```

**输出:**

```py
Expression : x**3*y**3 + x**2*y**2 + 2*x*y 
Derivative of expression with respect to x : Derivative(x**3*y**3 + x**2*y**2 + 2*x*y, x, y)
Value of the derivative : 9*x**2*y**2 + 4*x*y + 2 

```