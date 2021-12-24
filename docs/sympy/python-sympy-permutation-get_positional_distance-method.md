# Python | SymPy placement . get _ positional _ distance()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-get _ positional _ distance-method/](https://www.geeksforgeeks.org/python-sympy-permutation-get_positional_distance-method/)

**arrangement . get _ positional _ distance():get _ positional _ distance()**是一个 sympy Python 库函数，计算两个排列之间的位置距离。

> **语法:**
> sympy . combinations .排列.置换. get_positional_distance()
> 
> **返回:**
> 两个排列之间的位置距离

**代码#1 : get_positional_distance()示例**

```
# Python code explaining
# SymPy.Permutation.get_positional_distance()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.get_positional_distance() method 

# creating Permutation
a = Permutation([2, 0, 3, 1, 5, 4])

b = Permutation([3, 1, 2, 5, 4, 0])

c = Permutation([0, 1, 3, 4, 5, 2])

print ("a - get_positional_distance form b: ", a.get_positional_distance(b))
print ("b - get_positional_distance form c: ", b.get_positional_distance(c))
```

**输出:**

> a–获取位置距离表格 b:12
> b–获取位置距离表格 c: 8

**代码#2 : get_positional_distance()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.get_positional_distance()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.get_positional_distance() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [7, 1, 3],
                 [8, 5, 6]])

b = Permutation([[8, 4, 0], 
                 [2, 7, 0],
                 [1, 6, 7]])

print ("a get_positional_distance form b : ", a.get_positional_distance(b))
```

**输出:**

> 获取位置距离表格 b : 22