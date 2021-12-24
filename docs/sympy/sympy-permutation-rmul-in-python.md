# 友善|交换。rml()在 Python

中

> 原文:[https://www . geeksforgeeks . org/sympy-arrange-rmul-in-python/](https://www.geeksforgeeks.org/sympy-permutation-rmul-in-python/)

**置换. rmul() : rmul()** 是一个 sympy Python 库函数，返回置换的乘积。

> **语法:**sympy . combinations . arranges . arrange . rmul()
> 
> **返回:**排列的乘积。

**代码#1 : rmul()示例**

```
# Python code explaining
# SymPy.Permutation.rmul()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.rmul() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - rmul form : ", a.rmul(b))
print ("Permutation b - rmul form : ", b.rmul(a))
```

**输出:**

> 排列 a–rmul 形式:(0 1 3 4 2 5)
> 排列 b–rmul 形式:(0 2)(1 3)

**代码#2 : rmul()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.rmul()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.rmul() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - rmul form : ", a.rmul(a))
```

**输出:**

> 排列 a–rmul 形式:(0 3 5 6 1 2 4)