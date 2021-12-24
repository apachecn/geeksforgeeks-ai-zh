# Python | sympy.sqrt()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-sqrt-method-2/](https://www.geeksforgeeks.org/python-sympy-sqrt-method-2/)

借助 **sympy.sqrt()** 方法，我们可以用数值和符号化简化的数学表达式来求任意值的平方根。

> **语法:** sqrt(val)
> 
> **参数:**
> **val–**是要执行平方根运算的值。
> 
> **返回:**返回与输入表达式对应的值和符号化简化数学表达式的平方根。

**示例#1:**

```py
# import sympy 
from sympy import * 

val = 256

print("Value : {}".format(val)) 

# Use sympy.sqrt() method 
sqrt_val = sqrt(val)  

print("Square root of value : {}".format(sqrt_val))  
```

**输出:**

```py
Value : 256
Square root of value : 16

```

**例 2:**

```py
# import sympy 
from sympy import * 

val = 8

print("Value : {}".format(val)) 

# Use sympy.sqrt() method 
sqrt_val = sqrt(val)  

print("Square root of value : {}".format(sqrt_val))  
```

**输出:**

```py
Value : 8
Square root of value : 2*sqrt(2)

```