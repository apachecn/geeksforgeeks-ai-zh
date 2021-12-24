# Python 中的 SymPy | Subset.subset()

> 原文:[https://www . geesforgeks . org/sympy-subset-subset-in-python/](https://www.geeksforgeeks.org/sympy-subset-subset-in-python/)

**Subset.subset() : subset()** 是一个 sympy Python 库函数，返回当前实例表示的子集。

> **语法:**
> sympy . combinations . subset . subset . subset()
> 
> **返回:**
> 当前实例所代表的子集。

**代码#1:子集()示例**

```
# Python code explaining
# SymPy.Subset.subset()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.subset()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# subset value
print ("Subset a subset : ", a.subset)
```

**输出:**

> 子集 a 子集:['c '，' d']

**代码#2:子集()示例**

```
# Python code explaining
# SymPy.Subset.subset()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.subset()

# Creating Subset
a = Subset([2, 3, 4], [1, 2, 3, 4, 5])

# subset value
print ("Subset a subset : ", a.subset)
```

**输出:**

> 子集 a 子集:[2，3，4]