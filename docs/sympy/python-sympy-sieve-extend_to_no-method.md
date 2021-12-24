# Python sympy | screen . extend _ to _ no()方法

> 原文:[https://www . geesforgeks . org/python-sympy-screen-extend _ to _ no-method/](https://www.geeksforgeeks.org/python-sympy-sieve-extend_to_no-method/)

借助**sympy . screen . extend _ to _ no()**方法，我们可以将[筛](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes)扩展到包含带有素数的*。
**注意:**如果列表太短，会延长 50%，所以很可能会比请求的长。*

> **语法:**筛. extend_to_no(i)
> **参数:**
> **I–**表示筛扩展到包含第 I 个素数。
> **返回:**该方法不返回任何内容。

**示例#1:**

```py
# import sympy 
from sympy import sieve

# Use sieve.extend_to_no() method 
sieve.extend_to_no(15) 
prime_list = sieve._list

print("Prime Numbers up to 15th prime : {}".format(prime_list))  
```

**输出:**

```py
Prime Numbers up to 15th prime : array('l', [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61])

```

**例 2:**

```py
# import sympy 
from sympy import sieve

# Use sieve.extend_to_no() method 
sieve.extend_to_no(20) 
prime_list = sieve._list

print("Prime Numbers up to 15th prime : {}".format(prime_list))   
```

**输出:**

```py
Prime Numbers up to 15th prime : array('l', [2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89])

```