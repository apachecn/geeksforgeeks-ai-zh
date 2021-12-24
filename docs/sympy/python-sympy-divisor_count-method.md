# Python | sympy .除数 _count()方法

> 原文:[https://www . geesforgeks . org/python-sympy-divider _ count-method/](https://www.geeksforgeeks.org/python-sympy-divisor_count-method/)

借助 **sympy .除数 _count()** 方法，我们可以统计给定整数的除数。

> **语法:**除数 _ 计数(n，模=1)
> 
> **参数:**
> **n–**表示整数。
> **模数–**默认设置为 1。如果模数不是 1，那么只计算那些能被模数整除的。
> 
> **返回:**返回给定数的除数。

**示例#1:**

```
# import divisor_count() method from sympy
from sympy import divisor_count

n = 84

# Use divisor_count() method 
divisor_count_n = divisor_count(n) 

print("The number of divisors of {} : {}".format(n, divisor_count_n))
```

**输出:**

```
The number of divisors of 84 : 12

```

**例 2:**

```
# import divisor_count() method from sympy
from sympy import divisor_count

n = 12

# Use divisor_count() method 
divisor_count_n = divisor_count(n, modulus = 2) 

print("The number of divisors of {} : {}".format(n, divisor_count_n))
```

**输出:**

```
The number of divisors of 12 : 4

```