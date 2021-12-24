# 同情| prufer . prev()用 Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/symy-pruder-prev-in-python/

**Prufer.prev() : prev()** 是一个 sympy Python 库函数，返回当前序列之前的 delta 的 Prufer 序列。

> **语法:**
> 友好。组合者。prufer . prufer . prev()
> 
> **返回:**
> 当前序列之前的增量序列

**代码#1 : prev()示例**

```
# Python code explaining
# SymPy.Prufer.prev()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.prev()

# Creating Prufer
a = Prufer([1, 2, 3], [2, 4, 5])

# prev value
print ("Prufer a prev : ", a.prev(1))
```

**输出:**

> prufer a 预测:pruder([1，2，4])

**代码#2 : prev()示例**

```
# Python code explaining
# SymPy.Prufer.prev()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.prev()

# Creating Prufer
b = Prufer([1, 2, 3, 2, 4, 5], [6, 7], [8])

# prev value
print ("Prufer b prev : ", b.prev(1))
```

**输出:**

> 预测的缓冲区 b:缓冲区([1，2，3，2，4，4])