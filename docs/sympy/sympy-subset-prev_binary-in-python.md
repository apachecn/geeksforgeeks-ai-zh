# Python 中的 SymPy | Subset.prev_binary()

> 原文:[https://www . geesforgeks . org/sympy-subset-prev _ binary-in-python/](https://www.geeksforgeeks.org/sympy-subset-prev_binary-in-python/)

**subset . prev _ binary():prev _ binary()**是一个 sympy Python 库函数，返回之前的二进制有序子集。

> **语法:**
> sympy . combinations . subset . subset . prev _ binary()
> 
> **返回:**
> 之前的二进制有序子集。

**代码#1 : prev_binary()示例**

```
# Python code explaining
# SymPy.Subset.prev_binary()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.prev_binary()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# prev_binary value
print ("Subset a prev_binary : ", a.prev_binary().subset)
```

**输出:**

> 子集 a prev_binary : ['c']

**代码#2 : prev_binary()示例**

```
# Python code explaining
# SymPy.Subset.prev_binary()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.prev_binary()

# Creating Subset
a = Subset(['k', 'a'], ['23', 'k', 'a'])

# prev_binary value
print ("Subset a prev_binary : ", a.prev_binary().subset)
```

**输出:**

> 子集 a prev_binary : ['k']