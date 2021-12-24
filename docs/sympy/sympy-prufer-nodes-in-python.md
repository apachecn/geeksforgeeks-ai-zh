# Python 中的 SymPy | Prufer.nodes()

> 原文:[https://www.geeksforgeeks.org/sympy-prufer-nodes-in-python/](https://www.geeksforgeeks.org/sympy-prufer-nodes-in-python/)

**Prufer.nodes() : nodes()** 是一个 sympy Python 库函数，返回树中的节点数。

> **语法:**
> 友好。组合器. prufer . prufer . nodes()
> 
> **返回:**
> 树中的节点数

**代码#1:节点()示例**

```py
# Python code explaining
# SymPy.Prufer.nodes()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.nodes()

# Creating Prufer
a = Prufer([1, 2, 3], [2, 4, 5])

# nodes value
print ("Prufer a nodes : ", a.nodes)
```

**输出:**

> Prufer a 节点:5

**代码#2:节点()示例**

```py
# Python code explaining
# SymPy.Prufer.nodes()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.nodes()

# Creating Prufer
b = Prufer([1, 2, 3, 2, 4, 5], [6, 7], [8])

# nodes value
print ("Prufer b nodes : ", b.nodes)
```

**输出:**

> 普鲁士 b 节点:8 个