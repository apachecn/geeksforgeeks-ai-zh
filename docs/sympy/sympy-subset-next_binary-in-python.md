# Python 中的 SymPy | Subset.next_binary()

> 原文:[https://www . geesforgeks . org/sympy-subset-next _ binary-in-python/](https://www.geeksforgeeks.org/sympy-subset-next_binary-in-python/)

**subset . next _ binary():next _ binary()**是一个 sympy Python 库函数，返回下一个二进制有序子集。

> **语法:**
> sympy . combinations . subset . subset . next _ binary()
> 
> **返回:**
> 下一个二进制有序子集

**代码#1 : next_binary()示例**

```py
# Python code explaining
# SymPy.Subset.next_binary()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.next_binary()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# next_binary value
print ("Subset a next_binary : ", a.next_binary().subset)
```

**输出:**

> 子集 a next_binary : ['for']

**代码#2 : next_binary()示例**

```py
# Python code explaining
# SymPy.Subset.next_binary()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.next_binary()

# Creating Subset
a = Subset(['c', 'd'], ['23', 'c', 'd'])

# next_binary value
print ("Subset a next_binary : ", a.next_binary().subset)
```

**输出:**

> 子集 a next_binary : ['23']