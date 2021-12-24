# Python | sympy.nP()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-np-method/](https://www.geeksforgeeks.org/python-sympy-np-method/)

借助 **sympy.nP()** 方法，我们可以计算出给定长度在 sympy 中的置换数。

> **语法:** nP(项，k)
> 
> **参数:**
> **项–**要计算排列的整数、列表或字符串。
> **k–**指定排列长度的整数。
> 
> **返回:**返回给定长度的置换数。

**示例#1:**

```py
# import sympy 
from sympy import * 

items = "abca"
k = 3
print("Value of k = {} and the items are = {}".format(k, items))

# Use sympy.nP() method 
permutations = nP(items, k)  

print("Permutation : {}".format(permutations))  
```

**输出:**

```py
Value of k = 3 and the items are = abca
Permutation : 12

```

**例 2:**

```py
# import sympy 
from sympy import * 

items = [2, 1, 3, 5, 4]
k = 3
print("Value of k = {} and the items are = {}".format(k, items))

# Use sympy.nP() method 
permutations = nP(items, k)  

print("Permutation : {}".format(permutations))  
```

**输出:**

```py
Value of k = 3 and the items are = [2, 1, 3, 5, 4]
Permutation : 60

```