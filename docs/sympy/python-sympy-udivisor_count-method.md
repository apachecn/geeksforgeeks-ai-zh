# Python | sympy.udivisor_count()方法

> 原文:[https://www . geesforgeks . org/python-sympy-udi visor _ count-method/](https://www.geeksforgeeks.org/python-sympy-udivisor_count-method/)

借助 **sympy.udivisor_count()** 方法，我们可以统计给定整数的[酉除数](https://en.wikipedia.org/wiki/Unitary_divisor)的个数。

> **语法:** udivisor_count(n，模数=1)
> 
> **参数:**
> **n–**表示整数。
> 
> **返回:**返回给定整数的酉除数。

**示例#1:**

```py
# import divisor_count() method from sympy
from sympy.ntheory.factor_ import udivisor_count

n = 84

# Use udivisor_count() method 
udivisor_count_n = udivisor_count(n) 

print("The unitary number of divisors of {} : {}".format(n, udivisor_count_n))
```

**输出:**

```py
The unitary number of divisors of 84 : 8

```

**例 2:**

```py
# import divisor_count() method from sympy
from sympy.ntheory.factor_ import udivisor_count

n = 210

# Use udivisor_count() method 
udivisor_count_n = udivisor_count(n) 

print("The unitary number of divisors of {} : {}".format(n, udivisor_count_n))
```

**输出:**

```py
The unitary number of divisors of 210 : 16

```