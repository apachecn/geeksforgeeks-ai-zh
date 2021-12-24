# 同情| prufer . unrank()用 Python

> 原文:[https://www . geesforgeks . org/sympy-prufer-unlank-in-python/](https://www.geeksforgeeks.org/sympy-prufer-unrank-in-python/)

**Prufer . unlank():unlank()**是一个 sympy Python 库函数，返回未链接的 Prufer 序列。

> **语法:**
> 友好。组合者。prro fer . prro fer . un bank()
> 
> **返回:**
> 解开普鲁弗序列

**代码#1:未链接()示例**

```py
# Python code explaining
# SymPy.Prufer.unrank()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.unrank()

# Creating Prufer
a = Prufer([1, 2, 3], [2, 4, 5])

# unrank value
# rank = 2
# n = 5
print ("Prufer a unrank : ", a.unrank(2, 5))
```

**输出:**

> pruder a un bank:125

**代码#2:未链接()示例**

```py
# Python code explaining
# SymPy.Prufer.unrank()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.unrank()

# Creating Prufer
b = Prufer([1, 2, 3, 2, 4, 5], [6, 7], [8])

# unrank value
# rank = 2
# n = 5
print ("Prufer b unrank : ", b.unrank(2, 5))
```

**输出:**

> prfer b unbank:prfer([0，0，2])