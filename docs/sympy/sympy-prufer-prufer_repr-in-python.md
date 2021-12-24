# 友善|普鲁士人。普鲁士人 _repr()用 Python

> 吴奇珍:t0]https://www . geeksforgeeks . org/sympty-pruder-prfer _ repr-in-python/

**prufer . Prufer _ repr():Prufer _ repr()**是一个 sympy Python 库函数，返回 Prufer 对象的 Prufer 序列。通过移除编号最高的顶点，然后记录它所连接的节点，最后继续直到只剩下两个顶点，就可以找到序列。

> **语法:**
> 友好。组合者。普鲁士人。普鲁士人。普鲁士人 _repr()
> 
> **返回:**
> 普鲁弗对象的普鲁弗序列

**代码#1 : prufer_repr()示例**

```
# Python code explaining
# SymPy.Prufer.prufer_repr()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.prufer_repr()

# Creating Prufer
a = Prufer([1, 2, 3], [2, 4, 5])

# prufer_repr value
print ("Prufer a prufer_repr : ", a.prufer_repr)
```

**输出:**

> pruder 到 pruefer _ repr:[1，2，3]

**代码#2 : prufer_repr()示例**

```
# Python code explaining
# SymPy.Prufer.prufer_repr()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.prufer_repr()

# Creating Prufer
b = Prufer([1, 2, 3, 2, 4, 5], [6, 7], [8])

# prufer_repr value
print ("Prufer b prufer_repr : ", b.prufer_repr)
```

**输出:**

> prro b prro _ re:[1，2，3，2，4，5]