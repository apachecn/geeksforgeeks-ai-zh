# Python 中的 SymPy | Subset.rank_binary()

> 原文:[https://www . geesforgeks . org/sympy-subset-rank _ binary-in-python/](https://www.geeksforgeeks.org/sympy-subset-rank_binary-in-python/)

**subset . rank _ binary():rank _ binary()**是一个返回二进制有序秩的 sympy Python 库函数。

> **语法:**
> sympy . combinations . subset . subset . rank _ binary()
> 
> **返回:**
> 二进制有序秩。

**代码#1 : rank_binary()示例**

```py
# Python code explaining
# SymPy.Subset.rank_binary()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.rank_binary()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# rank_binary value
print ("Subset a rank_binary : ", a.rank_binary)
```

**输出:**

> 子集 a rank_binary : 3

**代码#2 : rank_binary()示例**

```py
# Python code explaining
# SymPy.Subset.rank_binary()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.rank_binary()

# Creating Subset
a = Subset([2, 3, 4], [1, 2, 3, 4, 5])

# rank_binary value
print ("Subset a rank_binary : ", a.rank_binary)
```

**输出:**

> 子集 a rank_binary : 14