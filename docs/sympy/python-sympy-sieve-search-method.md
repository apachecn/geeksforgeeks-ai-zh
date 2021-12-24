# Python 症状| screen . search()方法

> 原文:[https://www . geesforgeks . org/python-sympy-screen-search-method/](https://www.geeksforgeeks.org/python-sympy-sieve-search-method/)

借助**sympy . screen . search()**方法，我们可以找到束缚给定数的素数的指数 *i，j* 。如果给定的数是质数，那么 *i == j* 。

> **语法:**筛. search(n)
> **参数:**
> **n–**表示找到其有界素数索引的数。
> 
> **返回:**返回包含 **n** 的有界素数索引的元组。

**示例#1:**

```
# import sympy 
from sympy import sieve

# Use sieve.search() method 
i, j = sieve.search(23) 

print("The bounding prime indices of the number 23 : {}, {}".format(i, j))  
```

**输出:**

```
The bounding prime indices of the number 23 : 9, 9

```

**例 2:**

```
# import sympy 
from sympy import sieve

# Use sieve.search() method 
i, j = sieve.search(25) 

print("The bounding prime indices of the number 23 : {}, {}".format(i, j))      
```

**输出:**

```
The bounding prime indices of the number 23 : 9, 10

```