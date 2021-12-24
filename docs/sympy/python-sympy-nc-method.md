# Python | sympy.nC()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-nc-method/](https://www.geeksforgeeks.org/python-sympy-nc-method/)

借助 **sympy.nC()** 方法，可以计算出 sympy 中给定长度的组合个数。

> **语法:** nC(项，k)
> 
> **参数:**
> **项目–**要计算组合的整数、列表或字符串。
> **k–**指定组合长度的整数。
> 
> **返回:**返回给定长度的组合数。

**示例#1:**

```
# import sympy 
from sympy import * 

items = "abca"
k = 3
print("Value of k = {} and the items are = {}".format(k, items))

# Use sympy.nC() method 
combinations = nC(items, k)  

print("Combinations : {}".format(combinations))  
```

**输出:**

```
Value of k = 3 and the items are = abca
Combinations : 3

```

**例 2:**

```
# import sympy 
from sympy import * 

items = [2, 1, 3, 5, 4]
k = 3
print("Value of k = {} and the items are = {}".format(k, items))

# Use sympy.nC() method 
combinations = nC(items, k)  

print("Combinations : {}".format(combinations))  
```

**输出:**

```
Value of k = 3 and the items are = [2, 1, 3, 5, 4]
Combinations : 10

```