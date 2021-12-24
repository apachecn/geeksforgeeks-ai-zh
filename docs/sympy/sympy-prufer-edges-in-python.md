# 同情| prufer . edges()用 Python

表示

> 原文:[https://www.geeksforgeeks.org/sympy-prufer-edges-in-python/](https://www.geeksforgeeks.org/sympy-prufer-edges-in-python/)

**Prufer.edges() : edges()** 是一个 sympy Python 库函数，它返回给定运行中的节点数和边列表，这些节点连接到一个整数标记的树中的节点。

> **语法:**
> 友好。组合者。prufer . prufer . edges()
> 
> **返回:**
> 节点数和边列表

**代码#1:边()示例**

```py
# Python code explaining
# SymPy.Prufer.edges()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.edges()

# Creating Prufer
a = Prufer.edges([1, 2, 3], [2, 4, 5])

# edge value
print ("Prufer a edges : ", a)
```

**输出:**

> 测试边:([0.1]、[1.2]、[1.3]、[3.4]]、5)

**代码#2:边()示例**

```py
# Python code explaining
# SymPy.Prufer.edges()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.edges()

# Creating Prufer
b = Prufer.edges([1, 2, 3, 2, 4, 5], [6, 7], [8])

# edge value

print ("Prufer b edges : ", b)
```

**输出:**

> 普鲁士 b 边:([0.1]、[1.2]、[1.3]、[3.4]、[5.6]]、7)