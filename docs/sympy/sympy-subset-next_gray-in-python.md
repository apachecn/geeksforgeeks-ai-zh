# Python 中的 SymPy | Subset.next_gray()

> 原文:[https://www . geesforgeks . org/sympy-subset-next _ gray-in-python/](https://www.geeksforgeeks.org/sympy-subset-next_gray-in-python/)

**subset . next _ gray():next _ Gray()**是一个 sympy Python 库函数，返回下一个 Gray 码有序子集。

> **语法:**
> sympy . combinations . subset . subset . next _ gray()
> 
> **返回:**
> 下一个格雷码有序子集

**代码#1 : next_gray()示例**

```py
# Python code explaining
# SymPy.Subset.next_gray()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.next_gray()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# next_gray value
print ("Subset a next_gray : ", a.next_gray().subset)
```

**输出:**

> 子集 a next_gray : ['c']

**代码#2 : next_gray()示例**

```py
# Python code explaining
# SymPy.Subset.next_gray()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.next_gray()

# Creating Subset
a = Subset(['k', 'd'], ['23', 'k', 'd'])

# next_gray value
print ("Subset a next_gray : ", a.next_gray().subset)
```

**输出:**

> 子集 a next_gray : ['k']