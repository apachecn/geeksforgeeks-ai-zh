# Python 中的 SymPy | arrange . list()

> 原文:[https://www . geeksforgeeks . org/sympy-排列列表-in-python/](https://www.geeksforgeeks.org/sympy-permutation-list-in-python/)

**replacement . list():list()**是一个 sympy Python 库函数，它将置换作为显式列表返回，如果大小小于置换中的最大元素，可能会修剪不动的元素。

> **语法:**sympy . combinations .排列.置换. list()
> 
> **返回:**置换为显式列表

**代码#1:列表()示例**

```
# Python code explaining
# SymPy.Permutation.list()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.list() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - list form : ", a.list())
print ("Permutation b - list form : ", b.list())
```

**输出:**

> 排列 a–列表形式:[2，3，0，1]
> 排列 b–列表形式:[1，3，5，4，2，0]

**代码#2 : list()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.list()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.list() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - list form : ", a.list())
```

**输出:**

> 排列 a–列表形式:[3，2，4，5，0，6，1]