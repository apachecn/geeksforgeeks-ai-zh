# Python 中的症状|子集.超集()

> 原文:[https://www . geesforgeks . org/sympy-subset-super set-in-python/](https://www.geeksforgeeks.org/sympy-subset-superset-in-python/)

**subset . superset():superset()**是一个 sympy Python 库函数，返回子集的超集。

> **语法:**
> 症状.组合学.子集.子集.超集()
> 
> **返回:**
> 子集的超集。

**代码#1:超集()示例**

```py
# Python code explaining
# SymPy.Subset.superset()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.superset()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# superset value
print ("Subset a superset : ", a.superset)
```

**输出:**

> 子集 a 超集:['geek '，' for '，' c '，' d '

**代码#2:超集()示例**

```py
# Python code explaining
# SymPy.Subset.superset()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.superset()

# Creating Subset
a = Subset([2, 3, 4], [1, 2, 3, 4, 5])

# superset value
print ("Subset a superset : ", a.superset)
```

**输出:**

> 子集 a 超集:[1，2，3，4，5]