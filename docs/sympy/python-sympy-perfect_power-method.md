# Python | sympy.perfect_power()方法

> 原文:[https://www . geesforgeks . org/python-sympy-perfect _ power-method/](https://www.geeksforgeeks.org/python-sympy-perfect_power-method/)

借助 **sympy.perfect_power()** 方法，我们可以找到两个整数 ***b*** 和 ***e*** ，使得 ***b <sup>e</sup>*** 等于给定的数 ***n*** 。

> **句法:**
> 完成式 _ 幂(n)
> 
> **参数:**
> **n–**表示整数。
> 
> **返回:**
> 返回一个整数元组(b，e)，这样 b <sup>e</sup> == n。

**示例#1:**

```py
# import perfect_power() method from sympy
from sympy import perfect_power

n = 64

# Use perfect_power() method 
b, e = perfect_power(n) 

print("n = {}".format(n))
print("b = {} and e = {}.".format(b, e))
print("{}^{} == {}".format(b, e, n)) 
```

**输出:**

```py
n = 64
b = 2 and e = 6.
2^6 == 64

```

**例 2:**

```py
# import perfect_power() method from sympy
from sympy import perfect_power

n = 64

# Use perfect_power() method 
b, e = perfect_power(n, big = False) 

print("n = {}".format(n))
print("b = {} and e = {}.".format(b, e))
print("{}^{} == {}".format(b, e, n)) 
```

**输出:**

```py
n = 64
b = 8 and e = 2.
8^2 == 64

```