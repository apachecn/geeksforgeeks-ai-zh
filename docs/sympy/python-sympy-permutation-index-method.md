# Python | SymPy placement . index()方法

> 原文:[https://www . geesforgeks . org/python-sympy-排列-索引-方法/](https://www.geeksforgeeks.org/python-sympy-permutation-index-method/)

**arrange . index():index()**是一个 sympy Python 库函数，返回参数中排列的索引值。

**置换的索引=** 所有下标 j 的和，使得置换[j]大于置换[j+1]。

> **语法:**
> sympy . combinations .排列.置换. index()
> 
> **返回:**
> 排列的索引值

**代码#1:索引()示例**

```
# Python code explaining
# SymPy.Permutation.index()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.index() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - index form : ", a.index())
print ("Permutation b - index form : ", b.index())
```

**输出:**

> 排列 a–索引形式:1
> 排列 b–索引形式:9

**代码#2:索引()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.index()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.index() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - index form : ", a.index())
```

**输出:**

> 排列 a–索引形式:8