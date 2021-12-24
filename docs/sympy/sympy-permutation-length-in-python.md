# Python 中的 SymPy | arrange . length()

> 原文:[https://www . geesforgeks . org/sympy-置换-python 中的长度/](https://www.geeksforgeeks.org/sympy-permutation-length-in-python/)

**arrange . length():length()**是一个 sympy Python 库函数，用于查找由排列移动的整数个数。

> **语法:**sympy . combinations .排列.置换. length()
> 
> **返回:**排列移动的整数个数

**代码#1:长度()示例**

```py
# Python code explaining
# SymPy.Permutation.length()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.length() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - length form : ", a.length())
print ("Permutation b - length form : ", b.length())
```

**输出:**

> 排列 a-长度形式:4
> 排列 b-长度形式:6

**代码#2:长度()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.length()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.length() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - length form : ", a.length())
```

**输出:**

> 排列 a-长度形式:7