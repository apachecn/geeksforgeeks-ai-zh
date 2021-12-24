# Python | SymPy 置换. cardinality()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-基数-method/](https://www.geeksforgeeks.org/python-sympy-permutation-cardinality-method/)

**arrangement . cardinality():cardinality()**是一个 sympy Python 库函数，返回所有可能的排列个数。

> **语法:**sympy . combinations .排列.置换.基数()
> 
> **返回:**所有可能的排列数

**代码#1:基数()示例**

```py
# Python code explaining
# SymPy.Permutation.cardinality()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.cardinality() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - cardinality form : ", a.cardinality)
print ("Permutation b - cardinality form : ", b.cardinality)
```

**输出:**

> 排列 a–基数形式:24
> 排列 b–基数形式:720

**代码#2:基数()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.cardinality()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.cardinality() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - cardinality form : ", a.cardinality)
```

**输出:**

> 排列 a–基数形式:5040