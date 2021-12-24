# Python 中的 SymPy | subset . bitlist _ from _ subset()

> 原文:[https://www . geesforgeks . org/sympy-subset-bitlist _ from _ subset-in-python/](https://www.geeksforgeeks.org/sympy-subset-bitlist_from_subset-in-python/)

**subset . bit list _ from _ subset():bit list _ from _ subset()**是一个 sympy Python 库函数，返回子集对应的比特列表。

> **语法:**
> sympy . combinations . subset . subset . bitlist _ from _ subset()
> 
> **返回:**
> 对应子集的位列表

**代码#1 : bitlist_from_subset()示例**

```py
# Python code explaining
# SymPy.Subset.bitlist_from_subset()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.bitlist_from_subset()

# Creating Subset
a = Subset.bitlist_from_subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# bitlist_from_subset value
print ("Subset a bitlist_from_subset : ", a)
```

**输出:**

> 子集 a 位列表 _from_subset : 0011

**代码#2 : bitlist_from_subset()示例**

```py
# Python code explaining
# SymPy.Subset.bitlist_from_subset()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.bitlist_from_subset()

# Creating Subset
a = Subset.bitlist_from_subset(['1', '2'], ['4', '3', 'c', 'd'])

# bitlist_from_subset value
print ("Subset a bitlist_from_subset : ", a)
```

**输出:**

> 子集 a 位列表 _ 从 _ 子集:0000