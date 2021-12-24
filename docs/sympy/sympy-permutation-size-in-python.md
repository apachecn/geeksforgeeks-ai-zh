# Python 中的 SymPy | arrange . size()

> 原文:[https://www . geesforgeks . org/sympy-排列-python 中的大小/](https://www.geeksforgeeks.org/sympy-permutation-size-in-python/)

**arrange . size():size()**是一个 sympy Python 库函数，返回排列中的元素个数。

> **语法:**sympy . combinations .排列.置换. size()
> 
> **返回:**排列中的元素个数。

**代码#1:大小()示例**

```py
# Python code explaining
# SymPy.Permutation.size()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.size() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - size form : ", a.size)
print ("Permutation b - size form : ", b.size)
```

**输出:**

> 排列 a–大小形式:4
> 排列 b–大小形式:6

**代码#2:大小()示例**

```py
# Python code explaining
# SymPy.Permutation.size()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.size() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - size form : ", a.size)
```

**输出:**

> 排列 a-大小形式:7