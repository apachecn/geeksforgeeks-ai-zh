# 同情| prufer . rank()用 Python

表示

> 原文:[https://www.geeksforgeeks.org/sympy-prufer-rank-in-python/](https://www.geeksforgeeks.org/sympy-prufer-rank-in-python/)

**Prufer.rank() : rank()** 是一个 sympy Python 库函数，返回 Prufer 序列的秩。

> **语法:**
> 友好。组合者。普鲁士人。普鲁士人。rank()
> 
> **返回:**
> 普鲁弗序列的等级

**代码#1:排名()示例**

```py
# Python code explaining
# SymPy.Prufer.rank()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.rank()

# Creating Prufer
a = Prufer([1, 2, 3], [2, 4, 5])

# rank value
print ("Prufer a rank : ", a.rank)
```

**输出:**

> 普鲁士甲级联赛:38

**代码#2:排名()示例**

```py
# Python code explaining
# SymPy.Prufer.rank()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.rank()

# Creating Prufer
b = Prufer([1, 2, 3, 2, 4, 5], [6, 7], [8])

# rank value
print ("Prufer b rank : ", b.rank)
```

**输出:**

> 普鲁士 b 级:42661