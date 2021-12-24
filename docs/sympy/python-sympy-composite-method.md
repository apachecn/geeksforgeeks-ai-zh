# Python | sympy.composite()方法

> 原文:[https://www . geesforgeks . org/python-sympy-composite-method/](https://www.geeksforgeeks.org/python-sympy-composite-method/)

借助 **sympy.composite()** 方法，我们可以找到*第 n 个*复合数，复合数索引为*复合(1) = 4，复合(2) = 6* 等。

> **语法:**复合(n)
> 
> **参数:**
> **n–**表示第 n 个合成数。
> 
> **返回:**返回第 n 个合成数。

**示例#1:**

```py
# import sympy 
from sympy import composite

n = 5

# Use composite() method 
nth_composite = composite(n) 

print("The {}th composite is {}".format(n, nth_composite))  
```

**输出:**

```py
The 5th composite is 10

```

**例 2:**

```py
# import sympy 
from sympy import composite

n = 25

# Use composite() method 
nth_composite = composite(n) 

print("The {}th composite is {}".format(n, nth_composite))          
```

**输出:**

```py
The 25th composite is 38

```