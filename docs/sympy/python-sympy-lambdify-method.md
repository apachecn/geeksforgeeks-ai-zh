# Python | sympy.lambdify()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-lambdify-method/](https://www.geeksforgeeks.org/python-sympy-lambdify-method/)

借助 **sympy.lambdify()** 方法，我们可以将一个 *SymPy* 表达式转换成一个可以数值计算的表达式。 *lambdify* 的作用类似于 lambda 函数，只是它将 *SymPy* 的名称转换为给定数值库的名称，通常是 *NumPy* 或 *math* 。

> **语法:** lambdify(变量、表达式、库)
> 
> **参数:**
> **变量**–是数学表达式中的变量。
> **表达式**–是在给定的**库中转换成各自名称的数学表达式**。
> **库**–是**表达式**要转换到的 Python 库。
> 
> **返回:**返回一个可以计算数学表达式的λ函数。

**示例#1:**
在这个示例中，我们可以看到，通过使用 **sympy.lambdify()** 方法，我们可以从数学表达式中获得λ函数。

```py
# import sympy
from sympy import * 

x = symbols('x')
expr = sin(x)

# Use sympy.lambdify() method
f = lambdify(x, expr, "math") 

print("Using lambda function in SymPy to evaluate sin(90) : {}".format(f(90))) 
```

**输出:**

```py
Using lambda function in SymPy to evaluate sin(90) : 0.893996663601
```

**例 2:**
我们可以通过**sympy _ name:numeric _ function pair**的字典，对它不知道的数值库使用 lambdify。

```py
# import sympy
from sympy import * 

def squared(n) : 
    return n**2

x = symbols('x')
expr = x**2

# Use sympy.lambdify() method
f = lambdify(x, expr, {"**" : squared}) 

print("Using lambda function in SymPy to evaluate squared function : {}".format(f(10))) 
```

**输出:**

```py
Using lambda function in SymPy to evaluate squared function : 100

```