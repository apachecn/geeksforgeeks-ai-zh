# Python | SymPy placement . get _ preference _ distance()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-get _ preference _ distance-method/](https://www.geeksforgeeks.org/python-sympy-permutation-get_precedence_distance-method/)

**arrangement . get _ preference _ distance():get _ preference _ distance()**是一个 sympy Python 库函数，计算两个排列之间的优先距离。

p 和 q 代表 n 个作业。优先度量计算在 p 和 q 中作业 n 前面有作业 m 的次数。这是一个**交换矩阵**。

> **语法:**
> sympy . combinations .排列.置换. _ precedence _ distance()
> 
> **返回:**
> 两个排列之间的优先距离

**代码# 1:get _ preference _ distance()示例**

```py
# Python code explaining
# SymPy.Permutation.get_precedence_distance()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.get_precedence_distance() method 

# creating Permutation
a = Permutation([2, 0, 3, 1, 5, 4])

b = Permutation([3, 1, 2, 5, 4, 0])

c = Permutation([0, 1, 3, 4, 5, 2])

print ("a - get_precedence_distance form b: ", a.get_precedence_distance(b))
print ("b - get_precedence_distance form c: ", b.get_precedence_distance(c))
```

**输出:**

> a–get _ preference _ distance 表格 b:6
> b–get _ preference _ distance 表格 c: 9

**代码# 2:get _ preference _ distance()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.get_precedence_distance()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.get_precedence_distance() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [7, 1, 3],
                 [8, 5, 6]])

b = Permutation([[8, 4, 0], 
                 [2, 7, 0],
                 [1, 6, 7]])

print ("a get_precedence_distance form b : ", a.get_precedence_distance(b))
```

**输出:**

> a get _ precedence _ distance 表格 b : 22