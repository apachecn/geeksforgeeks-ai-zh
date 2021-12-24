# 友善|普鲁士人。tree_repr()用 Python

> 原文:[https://www . geesforgeks . org/sympy-prufer-tree _ repr-in-python/](https://www.geeksforgeeks.org/sympy-prufer-tree_repr-in-python/)

**Prufer . tree _ repr():tree _ repr()**是一个 sympy Python 库函数，返回 Prufer 序列的树表示。

> **语法:**
> 友好。组合者。普鲁士人。普鲁士人。tree_repr()
> 
> **返回:**
> 普鲁弗序列的树形表示

**代码#1 : tree_repr()示例**

```py
# Python code explaining
# SymPy.Prufer.tree_repr()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.tree_repr()

# Creating Prufer
a = Prufer([1, 2, 3], [2, 4, 5])

# tree_repr value
# rank = 2
# n = 5
print ("Prufer a tree_repr : ", a.tree_repr)
```

**输出:**

> 探测 tree _ repr:[[0.1]、[1.2]、[2.3]、[3.4]]

**代码#2 : tree_repr()示例**

```py
# Python code explaining
# SymPy.Prufer.tree_repr()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.tree_repr()

# Creating Prufer
b = Prufer([1, 2, 3, 2, 4, 5], [6, 7], [8])

# tree_repr value
# rank = 2
# n = 5
print ("Prufer b tree_repr : ", b.tree_repr)
```

**输出:**

> pruder b tree _ repr:[[0.1]、[1.2]、[3.6]、[2.3]、[2.4]、[4.5]、[5.7]]