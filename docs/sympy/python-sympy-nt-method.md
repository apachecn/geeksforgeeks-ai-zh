# Python | sympy.nT()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-nt-method/](https://www.geeksforgeeks.org/python-sympy-nt-method/)

借助 **sympy.nT()** 方法，我们可以计算出在 sympy 中可以有给定数量部分的分区数。

> **语法:** nT(项，k)
> 
> **参数:**
> **项目–**一个整数、一个列表或一个字符串，在此基础上计算分区。
> **k–**指定分区应包含的零件数量的整数。
> 
> **返回:**返回给定零件数的分区数。

**示例#1:**

```py
# import sympy 
from sympy import * 

items = "aaa"
k = 2

print("Value of k = {} and the items are = {}".format(k, items))

# Use sympy.nT() method 
partitions = nT(items, k)  

print("Partitions : {}".format(partitions))  
```

**输出:**

```py
Value of k = 2 and the items are = aaa
Partitions : 1

```

**例 2:**

```py
# import sympy 
from sympy import * 

items = [1, 3, 2, 5, 4]
k = 3
print("Value of k = {} and the items are = {}".format(k, items))

# Use sympy.nT() method 
partitions = nT(items, k)  

print("Partitions : {}".format(partitions))  
```

**输出:**

```py
Value of k = 3 and the items are = [1, 3, 2, 5, 4]
Partitions : 25

```