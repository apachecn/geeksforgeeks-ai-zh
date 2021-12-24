# Python 中的 SymPy | Prufer.to_tree()

> 原文:[https://www . geesforgeks . org/sympy-prufer-to _ tree-in-python/](https://www.geeksforgeeks.org/sympy-prufer-to_tree-in-python/)

**Prufer . to _ tree():to _ tree()**是一个 sympy Python 库函数，返回 Prufer 序列的树表示。

> **语法:**
> 友好。组合者。普鲁士人。普鲁士人。to_tree()
> 
> **返回:**
> 普鲁弗序列的表示

**代码#1 : to_tree()示例**

```py
# Python code explaining
# SymPy.Prufer.to_tree()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.to_tree()

# Creating Prufer
a = Prufer([1, 2, 3], [2, 4, 5], 4)

# to_tree value
print ("Prufer a to_tree : ", Prufer.to_tree([0, 2]))
```

**输出:**

> Prufer a to_tree : [[0，1]，[0，2]，[2，3]]

**代码#2 : to_tree()示例**

```py
# Python code explaining
# SymPy.Prufer.to_tree()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.to_tree()

# Creating Prufer
b = Prufer([1, 2, 3, 2, 4, 5], [6, 7], [8], 4)

# to_tree value
print ("Prufer b to_tree : ", Prufer.to_tree([0, 2]))
```

**输出:**

> Prufer b to_tree : [[0，1]，[0，2]，[2，3]]