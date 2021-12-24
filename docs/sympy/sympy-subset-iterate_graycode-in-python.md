# Python 中的 SymPy | Subset.iterate_graycode()

> 原文:[https://www . geesforgeks . org/sympy-subset-iterate _ gray code-in-python/](https://www.geeksforgeeks.org/sympy-subset-iterate_graycode-in-python/)

**subset . iterate _ Gray code():iterate _ Gray code()**是一个 sympy Python 库函数，它迭代 k 个步骤以获得各自的 Gray 码。

> **语法:**
> sympy . combinations . subset . subset . iterate _ gray code()
> 
> **返回:**
> 迭代 k 步得到各自的格雷码

**代码#1 : iterate_graycode()示例**

```py
# Python code explaining
# SymPy.Subset.iterate_graycode()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.iterate_graycode()

# Creating Subset
a = Subset(['c', 'd'], ['geek', 'for', 'c', 'd'])

# iterate_graycode value
print ("Subset a iterate_graycode : ", a.iterate_graycode(1).subset)
```

**输出:**

> 子集 a iterate_graycode : ['c']

**代码#2 : iterate_graycode()示例**

```py
# Python code explaining
# SymPy.Subset.iterate_graycode()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.subsets import Subset

# Using from 
# sympy.combinatorics.subset.Subsets.iterate_graycode()

# Creating Subset
a = Subset(['c', 'd'], ['23', 'c', 'd'])

# iterate_graycode value
print ("Subset a iterate_graycode : ", a.iterate_graycode(3).subset)
```

**输出:**

> 子集 a iterate_graycode : ['23 '，' c '，' d']