# Python 中的 SymPy | Subset.ksubsets()

> 原文:[https://www . geesforgeks . org/sympy-subset-ksubsets-in-python/](https://www.geeksforgeeks.org/sympy-subset-ksubsets-in-python/)

**subset . ksubsets():ksubsets()**是一个 sympy Python 库函数，按照字典顺序返回大小为 k 的子集。

> **语法:**
> sympy . combinations . subset . subset . ksubsets()
> 
> **返回:**
> 大小为 k 的子集按字典顺序排列。

**代码#1 : ksubsets()示例**

```py
# Python code explaining
# SymPy.Subset.ksubsets()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.ksubsets()

# Creating Subset
a = Subset.ksubsets(4, (['geek', 'for', 'c', 'd']))

# ksubsets value
print ("Subset a ksubsets : ", a.subset)
```

**输出:**

> 子集 a ksubsets : ['for '，' c']

**代码#2 : ksubsets()示例**

```py
# Python code explaining
# SymPy.Subset.ksubsets()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.ksubsets()

# Creating Subset
a = Subset.ksubsets(4, ([2, 3, 4]))

# ksubsets value
print ("Subset a ksubsets : ", a.subset)
```

**输出:**

> 子集 a k 子集:[2，3]