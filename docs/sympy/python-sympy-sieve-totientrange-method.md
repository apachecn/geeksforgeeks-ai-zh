# Python 症状|筛.全能性()方法

> 原文:[https://www . geesforgeks . org/python-sympy-screen-totilentrange-method/](https://www.geeksforgeeks.org/python-sympy-sieve-totientrange-method/)

借助**sympy . screen . totilentrange()**方法，我们可以为给定的范围**【a，b)** 生成所有的全能数。它返回一个类型生成器对象，该对象可以被转换为一个列表以供进一步操作。

> **语法:**筛. totilentrange(a，b)
> **参数:**
> **a–**它表示范围的开始。它是包容的。
> **b–**表示范围的终点。它不具有包容性。
> **返回:**该方法返回一个类型生成器对象。

**示例#1:**

```py
# import sympy 
from sympy import sieve

# Use sieve.totientrange() method 
totient_gen = sieve.totientrange(1, 10) 
totient_list = list(totient_gen)

print("Totient numbers for the range of numbers [1, 10) : {}".format(totient_list))  
```

**输出:**

```py
Totient numbers for the range of numbers [1, 10) : [1, 1, 2, 2, 4, 2, 6, 4, 6]

```

**例 2:**

```py
# import sympy 
from sympy import sieve

# Use sieve.totientrange() method 
totient_gen = sieve.totientrange(8, 20) 
totient_list = list(totient_gen)

print("Totient numbers for the range of numbers [8, 20) : {}".format(totient_list))      
```

**输出:**

```py
Totient numbers for the range of numbers [8, 20) : [4, 6, 4, 10, 4, 12, 6, 8, 8, 16, 6, 18]

```