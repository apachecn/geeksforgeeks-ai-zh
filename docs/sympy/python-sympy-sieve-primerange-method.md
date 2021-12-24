# Python sympy | screen . prime range()方法

> 原文:[https://www . geesforgeks . org/python-sympy-screen-prime range-method/](https://www.geeksforgeeks.org/python-sympy-sieve-primerange-method/)

借助**sympy . screen . prime range()**方法，我们可以生成给定范围**【a，b)** 的所有素数。它返回一个类型生成器对象，该对象可以被转换为一个列表以供进一步操作。

> **语法:**筛. primerange(a，b)
> **参数:**
> **a–**它表示范围的开始。它是包容的。
> **b–**表示范围的终点。它不具有包容性。
> **返回:**该方法返回一个类型生成器对象。

**示例#1:**

```
# import sympy 
from sympy import sieve

# Use sieve.primerange() method 
prime_gen = sieve.primerange(1, 10) 
prime_list = list(prime_gen)

print("Prime numbers for the range of numbers [1, 10) : {}".format(prime_list))  
```

**输出:**

```
Prime numbers for the range of numbers [1, 10) : [2, 3, 5, 7]

```

**例 2:**

```
# import sympy 
from sympy import sieve

# Use sieve.primerange() method 
prime_gen = sieve.primerange(8, 50) 
prime_list = list(prime_gen)

print("Prime numbers for the range of numbers [8, 50) : {}".format(prime_list))      
```

**输出:**

```
Prime numbers for the range of numbers [8, 50) : [11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47]

```