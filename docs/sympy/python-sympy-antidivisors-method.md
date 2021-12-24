# Python | sympy . antividus()方法

> 原文:[https://www . geesforgeks . org/python-sympy-antivisors-method/](https://www.geeksforgeeks.org/python-sympy-antidivisors-method/)

借助**sympy . antivisors()**方法，我们可以默认按照排序顺序找到给定数字的[除数](https://oeis.org/A066272/a066272a.html)。

> **语法:**解毒剂(n，生成器=假)
> 
> **参数:**
> **n–**表示整数。
> **生成器–**如果生成器为真，则返回一个无序的生成器对象，否则返回一个有序的除数列表。默认情况下为假。
> 
> **返回:**返回给定整数的除数列表。

**示例#1:**

```
# import antidivisors() method from sympy
from sympy.ntheory.factor_ import antidivisors

n = 24

# Use antidivisors() method 
antidivisors_n = antidivisors(n) 

print("The anti-divisors of {} : {}".format(n, antidivisors_n))
```

**输出:**

```
The anti-divisors of 24 : [7, 16]

```

**例 2:**

```
# import antidivisors() method from sympy
from sympy.ntheory.factor_ import antidivisors

n = 128

# Use antidivisors() method 
antidivisors_n = antidivisors(n) 

print("The anti-divisors of {} : {}".format(n, antidivisors_n))
```

**输出:**

```
The anti-divisors of 128 : [3, 5, 15, 17, 51, 85]

```