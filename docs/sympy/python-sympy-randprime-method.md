# Python | sympy.randprime()方法

> 原文:[https://www . geesforgeks . org/python-sympy-rand prime-method/](https://www.geeksforgeeks.org/python-sympy-randprime-method/)

借助 **sympy.randprime()** 方法，我们可以在***【a，b)*** 范围内找到一个随机素数，其中 ***a*** 和 ***b*** 是该方法的参数。

> **语法:** randprime(a，b)
> 
> **参数:**
> **a–**表示范围的开始。它是包容的。
> **b–**表示范围的结束。它不具有包容性。
> 
> **返回:**返回给定范围内的随机素数。如果该范围内没有质数，则引发值错误。

**示例#1:**

```py
# import randprime() method from sympy
from sympy import randprime

a = 4
b = 50

# Use randprime() method 
a_randprime_b = randprime(a, b) 

print("A random prime between {} and {} is {}".format(a, b, a_randprime_b))
```

**输出:**

```py
A random prime between 4 and 50 is 37

```

**例 2:**

```py
# import randprime() method from sympy
from sympy import randprime

a = 60
b = 100

# Use randprime() method 
a_randprime_b = randprime(a, b) 

print("A random prime between {} and {} is {}".format(a, b, a_randprime_b))          
```

**输出:**

```py
A random prime between 60 and 100 is 79

```