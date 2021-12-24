# Python 中的 SymPy | Subset.unrank _ binary()

> 原文:[https://www . geesforgeks . org/sympy-subset-unlank _ binary-in-python/](https://www.geeksforgeeks.org/sympy-subset-unrank_binary-in-python/)

**subset . unlank _ binary():unlank _ binary()**是一个 sympy Python 库函数，返回指定秩的二进制有序子集。

> **语法:**
> sympy . combinations . subset . subset . unlank _ binary()
> 
> **返回:**
> 指定秩的二进制有序子集。

**代码# 1:unlank _ binary()示例**

```py
# Python code explaining
# SymPy.Subset.unrank_binary()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.unrank_binary()

# Creating Subset
a = Subset.unrank_binary(4, (['geek', 'for', 'c', 'd']))

# unrank_binary value
print ("Subset a unrank_binary : ", a.subset)
```

**输出:**

> 子集 a unlank _ binary:[' for ']

**代码# 2:unlank _ binary()示例**

```py
# Python code explaining
# SymPy.Subset.unrank_binary()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.unrank_binary()

# Creating Subset
a = Subset.unrank_binary(4, ([2, 3, 4]))

# unrank_binary value
print ("Subset a unrank_binary : ", a.subset)
```

**输出:**

> 子集 a unlank _ binary:[2]