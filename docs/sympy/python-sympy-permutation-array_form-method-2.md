# Python | Sympy 排列()。数组 _ 形式法

> 原文:[https://www . geesforgeks . org/python-sympy-排列-array_form-method-2/](https://www.geeksforgeeks.org/python-sympy-permutation-array_form-method-2/)

借助`**sympy.combinatorics.Permutation().array_form**`方法，我们可以利用`sympy.combinatorics.Permutation().array_form`方法从多维数组或矩阵中得到线性数组。

> **语法:** `sympy.combinatorics.Permutation().array_form`
> 
> **返回:**返回一维数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.combinatorics.Permutation().array_form`方法，我们能够从矩阵或多维数组中获得线性数组。

```
# import sympy and Permutation
from sympy.combinatorics.permutations import Permutation
from sympy import * 

Permutation.print_cyclic = False

# Using sympy.combinatorics.partitions.Permutation().array_form method
gfg = Permutation([ [1, 2, 3], [21, 32, 44] ])

print(gfg.array_form)
```

**输出:**

> [0, 2, 3, 1, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 32, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 44, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 21]

**例 2 :**

```
# import sympy and Permutation
from sympy.combinatorics.permutations import Permutation
from sympy import * 

Permutation.print_cyclic = False

# Using sympy.combinatorics.partitions.Permutation().array_form method
gfg = Permutation([ [1, 2], [3, 4], [5] ])

print(gfg.array_form)
```

**输出:**

> [0, 2, 1, 4, 3, 5]