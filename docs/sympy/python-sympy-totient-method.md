# Python | sympy . totilent()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-totient-method/](https://www.geeksforgeeks.org/python-sympy-totient-method/)

借助**同余()**方法，我们可以求出给定整数的[欧拉同余函数或φ(n)](https://en.wikipedia.org/wiki/Euler%27s_totient_function)。欧拉全能函数是小于或等于给定整数且相对于它是素数的正整数的个数。换句话说，就是在***1<= k<= n***的范围内*T5【k】*的整数个数，其最大公约数 ***gcd(n，k)*** 等于 ***1*** 。

> **语法:**全图(n)
> 
> **参数:**
> **n–**表示整数。
> 
> **返回:**返回小于或等于该整数 n 的相对素数。

**示例#1:**

```py
# import totient() method from sympy
from sympy.ntheory.factor_ import totient

n = 24

# Use totient() method 
totient_n = totient(n) 

print("phi({}) =  {} ".format(n, totient_n)) # 1 5 7 11 13 17 19 23
```

**输出:**

```py
phi(24) =  8

```

**例 2:**

```py
# import totient() method from sympy
from sympy.ntheory.factor_ import totient

n = 19

# Use totient() method 
totient_n = totient(n) 

print("phi({}) =  {} ".format(n, totient_n))
```

**输出:**

```py
phi(19) =  18

```