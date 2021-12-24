# Python | sympy.powdenest()方法

> 原文:[https://www . geesforgeks . org/python-sympy-powden est-method-2/](https://www.geeksforgeeks.org/python-sympy-powdenest-method-2/)

借助 **sympy.powdenest()** 方法，我们可以使用以下等式转换数学表达式–

```py
 (x<sup>a</sup>)<sup>b</sup> = x<sup>ab</sup>
```

> **语法:** powdenest(表达式，力)
> 
> **参数:**
> **表达式**–需要转换的是数学表达式。
> **强制**–对于**表达式**来说，它应该总是等于 **true** 来转换，而不检查它们的有效性。
> 
> **返回:**返回与输入表达式对应的转换后的数学表达式。

**例#1:**
在这个例子中我们可以看到，通过使用 **sympy.powdenest()** 方法，我们可以用幂来转换一个数学表达式。

```py
# import sympy
from sympy import * 

x, a, b = symbols('x a b')
expr = (x**a)**b

print("Before Conversion : {}".format(expr))

# Use sympy.powdenest() method
smpl = powdenest(expr, force = true) 

print("After Conversion : {}".format(smpl)) 
```

**输出:**

```py
Before Conversion : (x**a)**b
After Conversion : x**(a*b)

```

**例 2:**

```py
# import sympy
from sympy import * 

x, a, b = symbols('x a b')
expr = (x**(a + b))**(a-b)

print("Before Conversion : {}".format(expr))

# Use sympy.powdenest() method
smpl = powdenest((x**(a + b))**(a-b), force = true) 

print("After Conversion : {}".format(smpl)) 
```

**输出:**

```py
Before Conversion : (x**(a + b))**(a - b)
After Conversion : x**((a - b)*(a + b))

```