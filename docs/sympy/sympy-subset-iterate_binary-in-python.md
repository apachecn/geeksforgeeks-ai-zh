# Python 中的 SymPy | Subset.iterate_binary()

> 原文:[https://www . geesforgeks . org/sympy-subset-iterate _ binary-in-python/](https://www.geeksforgeeks.org/sympy-subset-iterate_binary-in-python/)

**subset . iterate _ binary():iterate _ binary()**是一个 sympy Python 库函数，通过 k 步迭代二进制子集。“k”的值可以是正数，也可以是负数。

> **语法:**
> sympy . combinations . subset . subset . iterate _ binary()
> 
> **返回:**
> 以 k 步迭代二进制子集

**代码#1 : iterate_binary()示例**

```
# Python code explaining
# SymPy.Subset.iterate_binary()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.iterate_binary()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# iterate_binary value
print ("Subset a iterate_binary : ", a.iterate_binary(1).subset)
```

**输出:**

> 子集 a iterate_binary : ['for']

**代码#2 : iterate_binary()示例**

```
# Python code explaining
# SymPy.Subset.iterate_binary()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.iterate_binary()

# Creating Subset
a = Subset(['c', 'd'], ['23', 'c', 'd'])

# iterate_binary value
print ("Subset a iterate_binary : ", a.iterate_binary(2).subset)
```

**输出:**

> 子集 a iterate_binary : ['23 '，' d']