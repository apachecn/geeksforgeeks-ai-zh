# Python 中的 SymPy | Subset.rank_gray()

> 原文:[https://www . geesforgeks . org/sympy-subset-rank _ gray-in-python/](https://www.geeksforgeeks.org/sympy-subset-rank_gray-in-python/)

**subset . rank _ Gray():rank _ Gray()**是一个 sympy Python 库函数，返回子集的格雷码排名。

> **语法:**
> sympy . combinations . subset . subset . rank _ gray()
> 
> **返回:**
> 子集的格雷码排名

**代码#1 : rank_gray()示例**

```py
# Python code explaining
# SymPy.Subset.rank_gray()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.rank_gray()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# rank_gray value
print ("Subset a rank_gray : ", a.rank_gray)
```

**输出:**

> 子集 a 等级 _ 灰色:2

**代码#2 : rank_gray()示例**

```py
# Python code explaining
# SymPy.Subset.rank_gray()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.rank_gray()

# Creating Subset
a = Subset([2, 3, 4], [1, 2, 3, 4, 5])

# rank_gray value
print ("Subset a rank_gray : ", a.rank_gray)
```

**输出:**

> 子集 a 等级 _ 灰色:11