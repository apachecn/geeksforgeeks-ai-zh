# Python | sympy.crt()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-crt-method/](https://www.geeksforgeeks.org/python-sympy-crt-method/)

借助 **sympy.crt()** 方法，我们可以在 sympy 中实现[中国剩余定理](https://www.geeksforgeeks.org/chinese-remainder-theorem-set-1-introduction/)。

> **语法:** crt(m，v)
> 
> **参数:**
> **m–**表示整数列表。
> **v–**表示整数列表。
> 
> **返回:**返回一个整数元组，其中第一个元素是所需的结果。

**示例#1:**

```
# import crt() method from sympy
from sympy.ntheory.modular import crt

m = [5, 7]
v = [1, 3]

# Use crt() method 
crt_m_v = crt(m, v) 

print("Result of the Chinese Remainder Theorem = {} ".format(crt_m_v[0]))
```

**输出:**

```
Result of the Chinese Remainder Theorem = 31 

```

**例 2:**

```
# import crt() method from sympy
from sympy.ntheory.modular import crt

m = [99, 97, 95]
v = [49, 76, 65]

# Use crt() method 
crt_m_v = crt(m, v) 

print("Result of the Chinese Remainder Theorem = {} ".format(crt_m_v[0]))
```

**输出:**

```
Result of the Chinese Remainder Theorem = 639985 

```