# 好听|互换. mul_inv()用 Python

> 原文:[https://www . geesforgeks . org/sympy-置换-mul_inv-in-python/](https://www.geeksforgeeks.org/sympy-permutation-mul_inv-in-python/)

**arrangement . mul _ inv():mul _ inv()**是一个 sympy Python 库函数，返回 mul 逆 other*~self，self 和 other have _array_form。

> **语法:**sympy . combinations . arranges . arrangement . mul _ inv()
> 
> **返回:**mul 逆他者*~self，self 和 other 都有 _array_form。

**代码#1 : mul_inv()示例**

```
# Python code explaining
# SymPy.Permutation.mul_inv()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.mul_inv() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - mul_inv form : ", a.mul_inv(a))
print ("Permutation b - mul_inv form : ", b.mul_inv(b))
```

**输出:**

> 排列 a–mul _ inv 形式:(3)
> 排列 b–mul _ inv 形式:(5)

**代码#2 : mul_inv()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.mul_inv()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.mul_inv() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - mul_inv form : ", a.mul_inv(a))
```

**输出:**

> 排列 a–mul _ inv 形式:(6)