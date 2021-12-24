# Python 中的 SymPy | arrange . random()

> 原文:[https://www . geesforgeks . org/sympy-排列-python 中的随机/](https://www.geeksforgeeks.org/sympy-permutation-random-in-python/)

**replacement . random():random()**是一个 sympy Python 库函数，返回长度为‘n’的随机置换。

> **语法:**sympy . combinations .排列.置换. random()
> 
> **返回:**长度的随机排列

**代码#1:随机()示例**

```py
# Python code explaining
# SymPy.Permutation.random()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.random() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - random form : ", a.random(2))
print ("Permutation b - random form : ", b.random(5))
```

**输出:**

> 排列 a–随机形式:(1)
> 排列 b–随机形式:(4)

**代码#2:随机()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.random()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.random() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - random form : ", a.random(4))
```

**输出:**

> 排列 a–随机形式:(0 1 2 3)