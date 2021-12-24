# Python | sympy。积分()法

> 原文:[https://www.geeksforgeeks.org/python-sympy-integral-method/](https://www.geeksforgeeks.org/python-sympy-integral-method/)

借助**症状。Integral()** 方法，我们可以创建一个未赋值的 SymPy 表达式的积分。其语法与 **[integrate()](https://www.geeksforgeeks.org/python-sympy-integrate-method/)** 方法相同。要评估未评估的积分，请使用 **[doit()](https://www.geeksforgeeks.org/python-sympy-doit-method/)** 方法。

> **语法:**积分(表达式，引用变量)
> 
> **参数:**
> **表达式–**找到未赋值积分的一个 SymPy 表达式。
> **参考变量–**找到积分的变量。
> 
> **返回:**返回给定表达式的未赋值整数。

**示例#1:**

```py
# import sympy 
from sympy import * 

x, y = symbols('x y')
expr = x**2 + 2 * y + y**3
print("Expression : {} ".format(expr))

# Use sympy.Integral() method 
expr_intg = Integral(expr, x)  

print("Integral of expression with respect to x : {}".format(expr_intg))  
print("Value of the Integral : {} ".format(expr_intg.doit()))
```

**输出:**

```py
Expression : x**2 + y**3 + 2*y 
Integral of expression with respect to x : Integral(x**2 + y**3 + 2*y, x)
Value of the Integral : x**3/3 + x*(y**3 + 2*y) 

```

**例 2:**

```py
# import sympy 
from sympy import * 

x, y = symbols('x y')
expr = y**3 * x**2 + 2 * y*x + x * y**3
print("Expression : {} ".format(expr))

# Use sympy.Integral() method 
expr_intg = Integral(expr, x, y)  

print("Integral of expression with respect to x : {}".format(expr_intg))  
print("Value of the Integral : {} ".format(expr_intg.doit()))
```

**输出:**

```py
Expression : x**2*y**3 + x*y**3 + 2*x*y 
Integral of expression with respect to x : Integral(x**2*y**3 + x*y**3 + 2*x*y, x, y)
Value of the Integral : x**2*y**2/2 + y**4*(x**3/12 + x**2/8) 

```