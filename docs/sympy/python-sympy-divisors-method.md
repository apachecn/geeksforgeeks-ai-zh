# Python |症状因子()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-divisors-method/](https://www.geeksforgeeks.org/python-sympy-divisors-method/)

借助**约数()**方法，我们可以默认按排序顺序找到给定数的所有约数。

> **语法:**除数(n，生成器=假)
> 
> **参数:**
> **n–**表示整数。
> **生成器–**如果生成器为真，则返回一个无序的生成器对象，否则返回一个有序的除数列表。默认情况下为假。
> 
> **返回:**返回给定整数的所有除数的列表。

**示例#1:**

```py
# import divisors() method from sympy
from sympy import divisors

n = 84

# Use divisors() method 
divisors_n = divisors(n) 

print("The divisors of {} : {}".format(n, divisors_n))
```

**输出:**

```py
The divisors of 84 : [1, 2, 3, 4, 6, 7, 12, 14, 21, 28, 42, 84]

```

**例 2:**

```py
# import divisors() method from sympy
from sympy import divisors

n = -210

# Use divisors() method 
divisors_n = list(divisors(n, generator = True)) 

print("The divisors of {} : {}".format(n, divisors_n))
```

**输出:**

```py
The divisors of -210 : [1, 2, 3, 6, 5, 10, 15, 30, 7, 14, 21, 42, 35, 70, 105, 210]

```