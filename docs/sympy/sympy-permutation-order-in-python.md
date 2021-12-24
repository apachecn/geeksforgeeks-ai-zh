# Python 中的 SymPy | arrange . order()

> 原文:[https://www . geesforgeks . org/sympy-排列-python 中的顺序/](https://www.geeksforgeeks.org/sympy-permutation-order-in-python/)

**排列顺序() :顺序()**是一个计算排列顺序的 sympy Python 库函数。当置换被提升到它的阶的幂时，那么，在这种情况下，阶等于单位置换。

> **语法:**组合学.排列.排列.顺序()
> 
> **返回:**排列的顺序

**代码#1:订单()示例**

```
# Python code explaining
# SymPy.Permutation.order()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.order() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - order form : ", a.order())
print ("Permutation b - order form : ", b.order())
```

**输出:**

> 排列 a–顺序形式:2
> 排列 b–顺序形式:6

**代码#2:顺序()示例**–2D 排列

```
# Python code explaining
# SymPy.Permutation.order()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.order() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - order form : ", a.order())
```

**输出:**

> 排列 a–顺序形式:7