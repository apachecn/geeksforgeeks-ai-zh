# Python 中的 SymPy | Subset.size()

> 原文:[https://www.geeksforgeeks.org/sympy-subset-size-in-python/](https://www.geeksforgeeks.org/sympy-subset-size-in-python/)

**Subset.size() : size()** 是一个 sympy Python 库函数，返回子集的大小。

> **语法:**
> sympy . combinations . subset . subset . size()
> 
> **返回:**
> 子集的大小。

**代码#1:大小()示例**

```
# Python code explaining
# SymPy.Subset.size()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.size()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# size value
print ("Subset a size : ", a.size)
```

**输出:**

> 子集 a 大小:2

**代码#2:大小()示例**

```
# Python code explaining
# SymPy.Subset.size()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.size()

# Creating Subset
a = Subset([2, 3, 4], [1, 2, 3, 4, 5])

# size value
print ("Subset a size : ", a.size)
```

**输出:**

> 子集 a 大小:3