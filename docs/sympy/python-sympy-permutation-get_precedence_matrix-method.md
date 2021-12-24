# Python | SymPy placement . get _ preference _ matrix()方法

> 原文:[https://www . geeksforgeeks . org/python-sympy-置换-get _ preference _ matrix-method/](https://www.geeksforgeeks.org/python-sympy-permutation-get_precedence_matrix-method/)

**arrangement . get _ preference _ matrix():get _ preference _ matrix()**是一个 sympy Python 库函数，通过计算两者之间的优先距离来计算参数中排列的优先矩阵。

p 和 q 代表 n 个作业。优先度量计算在 p 和 q 中作业 n 前面有作业 m 的次数。这是一个**交换矩阵**。

> **语法:**
> sympy . combinations .排列.置换. _ precedence _ matrix()
> 
> **返回:**
> 计算置换的优先矩阵

**代码# 1:get _ preference _ matrix()示例**

```py
# Python code explaining
# SymPy.Permutation.get_precedence_matrix()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.get_precedence_matrix() method 

# creating Permutation
a = Permutation([2, 0, 3, 1, 5, 4])

b = Permutation([3, 1, 2, 5, 4, 0])

print ("a - get_precedence_matrix : \n", a.get_precedence_matrix())
print ("b - get_precedence_matrix : \n", b.get_precedence_matrix())
```

**输出:**

> a–get _ preference _ Matrix:
> Matrix([[0，1，0，1，1，1]，
> [0，0，0，0，1，1]，
> [1，1，0，1，1，1]，
> [0，1，0，0，1，1]，
> [0，0，0，0，0]，
> [0，0，0，0，1，0]])
> 
> b–get _ preference _ Matrix:
> Matrix([[0，0，0，0，0，0]，
> [1，0，1，0，1，1]，
> [1，0，0，0，1，1]，
> [1，1，1，0，1，1，1]，
> [1，0，0，0，0]，
> [1，0，0，0，1，0]])

**代码# 2:get _ preference _ matrix()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.get_precedence_matrix()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.get_precedence_matrix() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [7, 1, 3],
                 [8, 5, 6]])

b = Permutation([[8, 4, 0], 
                 [2, 7, 0],
                 [1, 6, 7]])

print ("a get_precedence_matrix : \n", a.get_precedence_matrix())

print ("\nb get_precedence_matrix : \n", b.get_precedence_matrix())
```

**输出:**

> a get _ preference _ Matrix:
> Matrix([[0，1，0，0，0，1，1，0，1]，
> [0，0，0，0，0，0，0，0]，
> [1，1，0，1，1，1，1，1，1]，
> [1，1，0，0，1，1，1，1]，
> [1，1，0，0，1，1，1，1]，【2】
> 
> b get _ preference _ Matrix:
> Matrix([[0，0，0，0，1，0，0，0]，
> [1，0，1，1，1，0，1，0]，
> [1，0，0，0，1，1，0，1，0]，
> [1，0，1，0，0，1，0，1，0]，
> [0，0，0，0，0，0，0，0，0，0，0，]