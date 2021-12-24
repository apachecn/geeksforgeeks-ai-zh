# Python 中的 SymPy | arrange . rank()

> 原文:[https://www . geeksforgeeks . org/sympy-置换-rank-in-python/](https://www.geeksforgeeks.org/sympy-permutation-rank-in-python/)

**arrange . rank():rank()**是一个 sympy Python 库函数，返回排列的字典排序。

> **语法:**sympy . combinations . arranges . arrange . rank()
> 
> **返回:**排列的字典顺序

**代码#1:排名()示例**

```py
# Python code explaining
# SymPy.Permutation.rank()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.rank() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - rank form : ", a.rank())
print ("Permutation b - rank form : ", b.rank())
```

**输出:**

> 排列 a–排列形式:16
> 排列 b–排列形式:191

**代码#2:秩()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.rank()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.rank() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - rank form : ", a.rank())
```

**输出:**

> 排列 a-等级形式:2461