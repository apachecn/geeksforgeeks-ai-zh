# Python | sympy.ff()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-ff-method/](https://www.geeksforgeeks.org/python-sympy-ff-method/)

借助 **sympy.ff()** 方法，我们可以找到[下降因子](http://mathworld.wolfram.com/FallingFactorial.html)。下降因子由–

![ ff(x, k) = x \cdot (x-1) \cdots (x-k+1) ](img/1772de4f352bab3342e573a8c996cba4.png "Rendered by QuickLaTeX.com")

其中 **x** 可以是任意表达式， **k** 是整数。

> **语法:** ff(x，k)
> 
> **参数:**
> **x–**表示任意表达式。
> **k–**表示整数。
> 
> **返回:**返回给定输入对应的下降因子。

**示例#1:**

```py
# import sympy 
from sympy import * 

x = symbols('x')
k = 5
print("Value of x = {} and k = {}".format(x, k))

# Use sympy.ff() method 
ff_x_k = ff(x, k)  

print("Falling factorial ff(x, k) : {}".format(ff_x_k))  
```

**输出:**

```py
Value of x = x and k = 5
Falling factorial ff(x, k) : x*(x - 4)*(x - 3)*(x - 2)*(x - 1)

```

**例 2:**

```py
# import sympy 
from sympy import * x = 7
k = 5
print("Value of x = {} and k = {}".format(x, k))

# Use sympy.ff() method 
ff_x_k = ff(x, k)  

print("Falling factorial ff(x, k) : {}".format(ff_x_k))  
```

**输出:**

```py
Value of x = 7 and k = 5
Falling factorial ff(x, k) : 2520

```