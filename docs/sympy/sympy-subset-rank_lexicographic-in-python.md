# Python 中的 SymPy | Subset.rank _ 词典学()

> 原文:[https://www . geesforgeks . org/sympy-subset-rank _ 词典编纂-in-python/](https://www.geeksforgeeks.org/sympy-subset-rank_lexicographic-in-python/)

**subset . rank _ dictionary():rank _ dictionary()**是一个 sympy Python 库函数，返回子集的字典排序。

> **语法:**
> sympy . combinations . subset . subset . rank _ dictionary graphic()
> 
> **返回:**
> 该子集的词典排名。

**代码# 1:rank _ dictionary()示例**

```py
# Python code explaining
# SymPy.Subset.rank_lexicographic()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.rank_lexicographic()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# rank_lexicographic value
print ("Subset a rank_lexicographic : ", a.rank_lexicographic)
```

**输出:**

> 子集 a 等级 _ 字典顺序:14

**代码# 2:rank _ dictionary()示例**

```py
# Python code explaining
# SymPy.Subset.rank_lexicographic()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.rank_lexicographic()

# Creating Subset
a = Subset([2, 3, 4], [1, 2, 3, 4, 5])

# rank_lexicographic value
print ("Subset a rank_lexicographic : ", a.rank_lexicographic)
```

**输出:**

> 子集 a 等级 _ 字典顺序:19