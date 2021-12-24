# Python 中的 SymPy | subset . prev _ dictionary graphic()

> 原文:[https://www . geesforgeks . org/sympy-subset-prev _ dictionary graphic-in-python/](https://www.geeksforgeeks.org/sympy-subset-prev_lexicographic-in-python/)

**subset . prev _ dictionary():prev _ dictionary()**是一个 sympy Python 库函数，返回之前的字典序子集。

> **语法:**
> sympy . combinations . subset . subset . prev _ dictionary graphic()
> 
> **返回:**
> 之前的格雷码有序子集。

**代码# 1:prev _ 词典()示例**

```
# Python code explaining
# SymPy.Subset.prev_lexicographic()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.prev_lexicographic()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# prev_lexicographic value
print ("Subset a prev_lexicographic : ", a.prev_lexicographic().subset)
```

**输出:**

> 子集 a prev _ 词典顺序:['c']

**代码# 2:prev _ 词典()示例**

```
# Python code explaining
# SymPy.Subset.prev_lexicographic()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.prev_lexicographic()

# Creating Subset
a = Subset([2, 3, 4], [1, 2, 3, 4, 5])

# prev_lexicographic value
print ("Subset a prev_lexicographic : ", a.prev_lexicographic().subset)
```

**输出:**

> 子集 a prev _ 字典顺序:[2，3]