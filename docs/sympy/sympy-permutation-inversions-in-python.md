# Python 中的 SymPy | Permutation.inversions()

> 原文:[https://www . geesforgeks . org/sympy-排列-倒置-in-python/](https://www.geeksforgeeks.org/sympy-permutation-inversions-in-python/)

**arrangement . inversion():inversion()**是一个 sympy Python 库函数，返回参数中置换的 inversion 个数值。
反转向量包括那些其值指示排列中的元素数量的元素，它们是<它并且位于它的右侧。

> **语法:**返回:参数中排列的逆序数值

**代码#1:反转()示例**

```py
# Python code explaining
# SymPy.Permutation.inversions()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.inversions() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - inversions form : ", a.inversions())
print ("Permutation b - inversions form : ", b.inversions())
```

**输出:**

> 排列 a–倒排形式:4
> 排列 b–倒排形式:9

**代码#2:反演()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.inversions()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.inversions() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - inversions form : ", a.inversions())
```

**输出:**

> 排列 a–倒排形式:10