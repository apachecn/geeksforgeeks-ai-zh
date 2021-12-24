# Python | sympy . antivisor _ count()方法

> 原文:[https://www . geesforgeks . org/python-sympy-antivisor _ count-method/](https://www.geeksforgeeks.org/python-sympy-antidivisor_count-method/)

借助**sympy . antivisor _ count()**方法，可以求出给定整数的[除数](https://oeis.org/A066272/a066272a.html)的个数。

> **语法:**antivisor _ count(n)
> 
> **参数:**
> **n–**表示整数。
> 
> **返回:**返回给定整数的除数。

**示例#1:**

```py
# import antidivisor_count() method from sympy
from sympy.ntheory.factor_ import antidivisor_count

n = 24

# Use antidivisor_count() method 
antidivisor_count_n = antidivisor_count(n) 

print("The number of anti-divisors of {} : {}".format(n, antidivisor_count_n))
```

**输出:**

```py
The number of anti-divisors of 24 : 2

```

**例 2:**

```py
# import antidivisor_count() method from sympy
from sympy.ntheory.factor_ import antidivisor_count

n = 128

# Use antidivisor_count() method 
antidivisor_count_n = antidivisor_count(n) 

print("The number of anti-divisors of {} : {}".format(n, antidivisor_count_n))
```

**输出:**

```py
The number of anti-divisors of 128 : 6

```