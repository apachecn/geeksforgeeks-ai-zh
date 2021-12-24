# Python | SymPy placement . get _ 邻接 _ 矩阵()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-get _ 邻接 _ 矩阵-method/](https://www.geeksforgeeks.org/python-sympy-permutation-get_adjacency_matrix-method/)

**arrangement . get _ 邻接矩阵():get _ 邻接矩阵()**是一个 sympy Python 库函数，计算自变量中置换的邻接矩阵。

> **语法:**
> sympy . combinations .排列.置换. get _ 邻接 _ 矩阵()
> 
> **返回:**
> 计算置换的邻接矩阵

**代码# 1:get _ 邻接矩阵()示例**

```
# Python code explaining
# SymPy.Permutation.get_adjacency_matrix()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.get_adjacency_matrix() method 

# creating Permutation
a = Permutation([2, 0, 3, 1, 5, 4])

b = Permutation([3, 1, 2, 5, 4, 0])

print ("a - get_adjacency_matrix : \n", a.get_adjacency_matrix())
print ("b - get_adjacency_matrix : \n", b.get_adjacency_matrix())
```

**输出:**

> a–get _ 邻接 _ 矩阵:
> 矩阵([[0，0，0，1，0，0]，
> [0，0，0，0，0，1]，
> [1，0，0，0，0，0]，
> [0，1，0，0，0，0，0]，
> [0，0，0，0，0，]，
> [0，0，0，0，0，1，0])
> 
> b–get _ 邻接 _ 矩阵:
> 矩阵([[0，0，0，0，0，0]，
> [0，0，1，0，0，0]，
> [0，0，0，0，0，1]，
> [0，1，0，0，0，0，0]，
> [1，0，0，0，0，0]，
> [0，0，0，0，0，1，0]])

**代码# 2:get _ 邻接矩阵()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.get_adjacency_matrix()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.get_adjacency_matrix() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [7, 1, 3],
                 [8, 5, 6]])

b = Permutation([[8, 4, 0], 
                 [2, 7, 0],
                 [1, 6, 7]])

print ("a get_adjacency_matrix : \n", a.get_adjacency_matrix())

print ("\nb get_adjacency_matrix : \n", b.get_adjacency_matrix())
```

**输出:**

> 一个 get _ 邻接 _ 矩阵:
> 矩阵([[0，0，0，0，0，0，1，0，0]，
> [0，0，0，0，0，0，0，]，
> [0，0，0，1，0，0，0，0，0，]，
> [0，0，0，0，0，0，1，0，0，0，0，]，
> [0，0，0，0，0，0，0，0，1，0]，【2】
> 
> b get _ 邻接 _ 矩阵:
> 矩阵([[0，0，0，0，1，0，0，0，0]，
> [0，0，0，1，0，0，0，0，0]，
> [0，0，0，0，0，1，0，0，0]，
> [0，0，1，0，0，0，0，0，0，0]，
> [0，0，0，0，0，0，0，0，0，0，0，0，0，]，【0