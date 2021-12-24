# Python 中的 SymPy | Subset.unrank _ gray()

> 原文:[https://www . geesforgeks . org/sympy-subset-unlank _ gray-in-python/](https://www.geeksforgeeks.org/sympy-subset-unrank_gray-in-python/)

**subset . unrank _ Gray():unrank _ Gray()**是一个 sympy Python 库函数，返回指定秩的格雷码有序子集。

> **语法:**
> sympy . combinations . subset . subset . unlank _ gray()
> 
> **返回:**
> 指定秩的格雷码有序子集。

**代码# 1:unlank _ gray()示例**

```
# Python code explaining
# SymPy.Subset.unrank_gray()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.unrank_gray()

# Creating Subset
a = Subset.unrank_gray(4, (['geek', 'for', 'c', 'd']))

# unrank_gray value
print ("Subset a unrank_gray : ", a.subset)
```

**输出:**

> 子集 a unrank_gray : ['代表'，' c']

**代码# 2:unlank _ gray()示例**

```
# Python code explaining
# SymPy.Subset.unrank_gray()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.unrank_gray()

# Creating Subset
a = Subset.unrank_gray(4, ([2, 3, 4]))

# unrank_gray value
print ("Subset a unrank_gray : ", a.subset)
```

**输出:**

> 子集 a unrank_gray : [2，3]