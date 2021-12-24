# Python 症状| screen . extend()方法

> 原文:[https://www . geesforgeks . org/python-sympy-screen-extend-method/](https://www.geeksforgeeks.org/python-sympy-sieve-extend-method/)

借助**sympy . screen . extend()**方法，我们可以增长[筛](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes)来覆盖所有小于等于给定自然数的素数。

> **语法:**筛.扩展(N)
> **参数:**
> **N–**表示筛扩展到的数量。
> **返回:**函数不返回任何内容。

**示例#1:**

```
# import sympy 
from sympy import sieve

# Use sieve.extend() method 
sieve.extend(50) 
prime_list = sieve._list

print("Prime Numbers up to 50 : {}".format(prime_list))  
```

**输出:**

```
Prime Numbers up to 50 : array('l', [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47])

```

**例 2:**

```
# import sympy 
from sympy import sieve

# Use sieve.extend() method 
sieve.extend(100) 
prime_list = sieve._list

print("Prime Numbers up to 100 : {}".format(prime_list))  
```

**输出:**

```
Prime Numbers up to 100 : array('l', [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97])

```