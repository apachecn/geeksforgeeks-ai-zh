# 友善|普鲁士人. to _ prufer()在 Python

中

> 原文:[https://www . geesforgeks . org/sympy-prufer-to _ prufer-in-python/](https://www.geeksforgeeks.org/sympy-prufer-to_prufer-in-python/)

**Prufer . to _ Prufer():to _ Prufer()**是一个 sympy Python 库函数，它返回一个参数树的 Prufer 序列，该序列以边列表的形式给出， **n** 是树中的节点数。

> **语法:**
> 友好。组合者。普鲁士人。普鲁士人。to _ prufer()
> 
> **返回:**
> 议论文树的普鲁弗序列

**代码#1 : to_prufer()示例**

```py
# Python code explaining
# SymPy.Prufer.size()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.size()

# Creating Prufer
a = Prufer([1, 2, 3], [2, 4, 5])

# size value
print ("Prufer a size : ", a.to_prufer([[0, 1], [0, 2], [0, 3]], 4))
```

**输出:**

> 校样大小:[0，0]

**代码#2 : to_prufer()示例**

```py
# Python code explaining
# SymPy.Prufer.size()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.size()

# Creating Prufer
b = Prufer([1, 2, 3, 2, 4, 5], [6, 7], [8])

# size value
print ("Prufer b size : ", b.to_prufer([[0, 1], [0, 2], [0, 3]], 4))
```

**输出:**

> 普鲁士 b 大小:[0，0]