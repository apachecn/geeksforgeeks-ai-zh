# Python 中的症状|子集.子集 _ 索引()

> 原文:[https://www . geesforgeks . org/sympy-subset-subset _ indexs-in-python/](https://www.geeksforgeeks.org/sympy-subset-subset_indices-in-python/)

**subset . subset _ indexes():subset _ indexes()**是一个 sympy Python 库函数，返回列表中超集中子集的索引

> **语法:**
> sympy . combinations . subset . subset . subset _ indexs()
> 
> **如果子集的所有元素都不在超集中，则返回:**
> 列表中超集中子集的索引
> 。–列表为空

**代码#1:子集 _ 索引()示例**

```py
# Python code explaining
# SymPy.Subset.subset_indices()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.subset_indices()

# superset
super_set = [4, 3, 2, 7]

# Creating Subset
a = Subset.subset_indices((['geek', 'for', 'c', 'd']), super_set)

# subset_indices value
print ("Subset a subset_indices : ", a)
```

**输出:**

> 子集 a 子集 _ 索引:[]

**代码#2:子集 _ 索引()示例**

```py
# Python code explaining
# SymPy.Subset.subset_indices()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.subset_indices()

# superset
super_set = [4, 3, 2, 7]

# Creating Subset
a = Subset.subset_indices(([2, 3, 4]), super_set)

# subset_indices value
print ("Subset a subset_indices : ", a)
```

**输出:**

> 子集 a 子集 _ 索引:[2，1，0]