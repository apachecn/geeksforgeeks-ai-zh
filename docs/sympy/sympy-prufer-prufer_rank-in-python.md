# 友善|普鲁士人。普鲁士人 _rank()用 Python

> 吴奇珍:t0]https://www . geeksforgeeks . org/sympty-pruder-prfer _ rank-in-python/

**Prufer . Prufer _ rank():Prufer _ rank()**是一个 sympy Python 库函数，用于计算一个 Prufer 序列的秩

> **语法:**
> 友好。组合者。普鲁士人。普鲁士人。普鲁士人 _rank()
> 
> **返回:**
> 普鲁弗序列的等级

**代码#1 : prufer_rank()示例**

```py
# Python code explaining
# SymPy.Prufer.prufer_rank()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.prufer_rank()

# Creating Prufer
a = Prufer([1, 2, 3], [2, 4, 5])

# prufer_rank value
print ("Prufer a prufer_rank : ", a.prufer_rank())
```

**输出:**

> pruder 到 pruefer _ rank:38

**代码#2 : prufer_rank()示例**

```py
# Python code explaining
# SymPy.Prufer.prufer_rank()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.prufer import Prufer

# Using from 
# sympy.combinatorics.prufer.Prufer.prufer_rank()

# Creating Prufer
b = Prufer([1, 2, 3, 2, 4, 5], [6, 7], [8])

# prufer_rank value
print ("Prufer b prufer_rank : ", b.prufer_rank())
```

**输出:**

> pruder b pruder _ rank:42661