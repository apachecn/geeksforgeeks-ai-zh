# 同情| prufer . size()用 Python

表示

> 原文:[https://www.geeksforgeeks.org/sympy-prufer-size-in-python/](https://www.geeksforgeeks.org/sympy-prufer-size-in-python/)

**Prufer.size() : size()** 是一个 sympy Python 库函数，返回 Prufer 序列的大小。

> **语法:**
> 友好。组合体. prufer . prufer . size()
> 
> **返回:**
> 普鲁弗序列的大小

**代码#1:大小()示例**

```
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
print ("Prufer a size : ", a.size)
```

**输出:**

> 冲浪者 a 尺寸:125

**代码#2:大小()示例**

```
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
print ("Prufer b size : ", b.size)
```

**输出:**

> 普鲁士 b 尺寸:262144