# Python 中的 SymPy | Subset.cardinality()

> 原文:[https://www . geesforgeks . org/sympy-subset-cardinality-in-python/](https://www.geeksforgeeks.org/sympy-subset-cardinality-in-python/)

**subset . cardinality():cardinality()**是一个 sympy Python 库函数，返回所有可能子集的数量。

> **语法:**
> sympy . combinations . subset . subset . cardinality()
> 
> **返回:**
> 所有可能子集的数量

**代码#1:基数()示例**

```
# Python code explaining
# SymPy.Subset.cardinality()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.cardinality()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# cardinality value
print ("Subset a cardinality : ", a.cardinality)
```

**输出:**

> 子集 a 基数:16

**代码#2:基数()示例**

```
# Python code explaining
# SymPy.Subset.cardinality()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.cardinality()

# Creating Subset
a = Subset(['c', 'd'], ['23', 'c', 'd'])

# cardinality value
print ("Subset a cardinality : ", a.cardinality)
```

**输出:**

> 子集 a 基数:8