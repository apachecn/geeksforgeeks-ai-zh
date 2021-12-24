# Python 中的症状|子集.超集 _ 大小()

> 原文:[https://www . geesforgeks . org/sympy-subset-superset _ size-in-python/](https://www.geeksforgeeks.org/sympy-subset-superset_size-in-python/)

**subset . superset _ size():superset _ size()**是一个 sympy Python 库函数，返回超集的大小。

> **语法:**
> sympy . combinations . subset . subset . superset _ size()
> 
> **返回:**
> 超集的大小。

**代码#1:超集 _ 大小()示例**

```
# Python code explaining
# SymPy.Subset.superset_size()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.superset_size()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# superset_size value
print ("Subset a superset_size : ", a.superset_size)
```

**输出:**

> 子集 a 超集大小:4

**代码#2:超集 _ 大小()示例**

```
# Python code explaining
# SymPy.Subset.superset_size()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.superset_size()

# Creating Subset
a = Subset([2, 3, 4], [1, 2, 3, 4, 5])

# superset_size value
print ("Subset a superset_size : ", a.superset_size)
```

**输出:**

> 子集 a 超集大小:5