# Python | SymPy placement . get _ 邻接 _ 距离()方法

> 原文:[https://www . geeksforgeeks . org/python-sympy-置换-get _ 邻接 _ 距离-method/](https://www.geeksforgeeks.org/python-sympy-permutation-get_adjacency_distance-method/)

**arrangement . get _ 邻接 _ distance():get _ 邻接 _distance()** 是一个计算两个置换之间邻接距离的 sympy Python 库函数。

> **语法:**
> sympy . combinations .排列.置换. get _ 邻接 _distance()
> 
> **返回:**
> 两个排列之间的邻接距离

**代码# 1:get _ 邻接 _ 距离()示例**

```py
# Python code explaining
# SymPy.Permutation.get_adjacency_distance()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.get_adjacency_distance() method 

# creating Permutation
a = Permutation([2, 0, 3, 1, 5, 4])

b = Permutation([3, 1, 2, 5, 4, 0])

c = Permutation([0, 1, 3, 4, 5, 2])

print ("a - get_adjacency_distance form b: ", a.get_adjacency_distance(b))
print ("b - get_adjacency_distance form c: ", b.get_adjacency_distance(c))
```

**输出:**

> a–get _ 邻接 _ 距离表格 b:3
> b–get _ 邻接 _ 距离表格 c: 5

**代码# 2:get _ 邻接 _ 距离()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.get_adjacency_distance()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.get_adjacency_distance() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [7, 1, 3],
                 [8, 5, 6]])

b = Permutation([[8, 4, 0], 
                 [2, 7, 0],
                 [1, 6, 7]])

print ("a get_adjacency_distance form b : ", a.get_adjacency_distance(b))
```

**输出:**

> a get _ 邻接 _ 距离形式 b : 7