# Python 中的 SymPy | subset . next _ dictionary()

> 原文:[https://www . geesforgeks . org/sympy-subset-next _ 词典编纂-in-python/](https://www.geeksforgeeks.org/sympy-subset-next_lexicographic-in-python/)

**subset . next _ dictionary():next _ dictionary()**是一个 sympy Python 库函数，返回下一个字典序子集。

> **语法:**
> sympy . combinations . subset . subset . next _ 词典学()
> 
> **返回:**
> 下一个字典序子集

**代码# 1:next _ 词典()示例**

```py
# Python code explaining
# SymPy.Subset.next_lexicographic()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.next_lexicographic()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# next_lexicographic value
print ("Subset a next_lexicographic : ", a.next_lexicographic().subset)
```

**输出:**

> 子集 a next _ 词典顺序:['d']

**代码# 2:next _ 词典()示例**

```py
# Python code explaining
# SymPy.Subset.next_lexicographic()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.next_lexicographic()

# Creating Subset
a = Subset(['k', 'a'], ['23', 'k', 'a'])

# next_lexicographic value
print ("Subset a next_lexicographic : ", a.next_lexicographic().subset)
```

**输出:**

> 子集 a next _ 词典顺序:['a']