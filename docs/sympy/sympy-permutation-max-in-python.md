# Python 中的 SymPy | arrange . max()

> 原文:[https://www . geesforgeks . org/sympy-置换-max-in-python/](https://www.geeksforgeeks.org/sympy-permutation-max-in-python/)

**置换. max() : max()** 是一个 sympy Python 库函数，返回置换中的最大值。

> **语法:**sympy . combinations . arranges . arrange . max()
> 
> **返回:**排列中的最大值。

**代码#1:最大值()示例**

```
# Python code explaining
# SymPy.Permutation.max()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.max() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - max form : ", a.max())
print ("Permutation b - max form : ", b.max())
```

**输出:**

> 排列 a–最大形式:3
> 排列 b–最大形式:5

**代码#2 : max()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.max()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.max() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - max form : ", a.max())
```

**输出:**

> 排列 a–最大形式:6