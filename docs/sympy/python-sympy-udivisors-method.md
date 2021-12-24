# Python | sympy . udvisors()方法

> 原文:[https://www . geesforgeks . org/python-sympy-udi visors-method/](https://www.geeksforgeeks.org/python-sympy-udivisors-method/)

借助 **sympy.udivisors()** 方法，我们可以默认按照排序顺序找到给定数的所有[酉除数](https://en.wikipedia.org/wiki/Unitary_divisor)。

> **语法:** udivisors(n，生成器=False)
> 
> **参数:**
> **n–**表示整数。
> **生成器–**如果生成器为真，则返回一个无序的生成器对象，否则返回一个酉除数的排序列表。默认情况下为假。
> 
> **返回:**返回给定整数的所有幺正除数的列表。

**示例#1:**

```
# import udivisors() method from sympy
from sympy.ntheory.factor_ import udivisors

n = 84

# Use udivisors() method 
udivisors_n = udivisors(n) 

print("The unitary divisors of {} : {}".format(n, udivisors_n))
```

**输出:**

```
The unitary divisors of 84 : [1, 3, 4, 7, 12, 21, 28, 84]

```

**例 2:**

```
# import udivisors() method from sympy
from sympy.ntheory.factor_ import udivisors

n = -210

# Use udivisors() method 
udivisors_n = list(udivisors(n, generator = True)) 

print("The unitary divisors of {} : {}".format(n, udivisors_n))
```

**输出:**

```
The unitary divisors of -210 : [1, 2, 3, 6, 5, 10, 15, 30, 7, 14, 21, 42, 35, 70, 105, 210]

```