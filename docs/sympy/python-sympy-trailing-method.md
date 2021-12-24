# Python | sympy . training()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-trailing-method/](https://www.geeksforgeeks.org/python-sympy-trailing-method/)

借助**sympy . training()**方法，我们可以统计给定数的二进制表示中的尾随零位数，即确定除以该数的 2 的最大幂。

> **语法:**
> 拖尾(n)
> 
> **参数:**
> **n–**它表示确定 2 的最大幂次除以该数的数。
> 
> **返回:**
> 返回给定数除以 2 的最大幂。

**示例#1:**

```
# import trailing() method from sympy
from sympy.ntheory.factor_ import trailing

n = 64

# Use trailing() method 
trailing_n = trailing(n) 

print("The largest power of 2 that divides {} is 2^{}.".
      format(n, trailing_n))
```

**输出:**

```
The largest power of 2 that divides 64 is 2^6.

```

**例 2:**

```
# import trailing() method from sympy
from sympy.ntheory.factor_ import trailing

n = 130

# Use trailing() method 
trailing_n = trailing(n) 

print("The largest power of 2 that divides {} is 2^{}.".
      format(n, trailing_n))
```

**输出:**

```
The largest power of 2 that divides 130 is 2^1.

```