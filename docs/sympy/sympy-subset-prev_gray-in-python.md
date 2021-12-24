# Python 中的 SymPy | Subset.prev_gray()

> 原文:[https://www . geesforgeks . org/sympy-subset-prev _ gray-in-python/](https://www.geeksforgeeks.org/sympy-subset-prev_gray-in-python/)

**subset . prev _ gray():prev _ Gray()**是一个 sympy Python 库函数，返回之前的 Gray 码有序子集。

> **语法:**
> sympy . combinations . subset . subset . prev _ gray()
> 
> **返回:**
> 之前的格雷码有序子集。

**代码#1 : prev_gray()示例**

```
# Python code explaining
# SymPy.Subset.prev_gray()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.prev_gray()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# prev_gray value
print ("Subset a prev_gray : ", a.prev_gray().subset)
```

**输出:**

> 子集 a prev_gray : ['d']

**代码#2 : prev_gray()示例**

```
# Python code explaining
# SymPy.Subset.prev_gray()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.prev_gray()

# Creating Subset
a = Subset([2, 3, 4], [1, 2, 3, 4, 5])

# prev_gray value
print ("Subset a prev_gray : ", a.prev_gray().subset)
```

**输出:**

> 子集 a prev_gray : [2，3，4，5]