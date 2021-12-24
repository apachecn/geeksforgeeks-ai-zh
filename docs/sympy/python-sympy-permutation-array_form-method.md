# Python | SymPy placement . array _ form()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-array_form-method/](https://www.geeksforgeeks.org/python-sympy-permutation-array_form-method/)

 **arrangement . array _ form():array _ form()**是一个 sympy Python 库函数，返回有论证的数组的一维副本。

> **语法:**sympy . combinations . arranges . array _ form()
> 
> **返回:**参数中置换的副本。

**代码#1 : array_form()示例**

```
# Python code explaining
# SymPy.array_form()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.array_form() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - array form : ", a.array_form)
print ("Permutation b - array form : ", b.array_form)
```

**输出:**

> 排列 a–数组形式:[2，3，0，1]
> 排列 b–数组形式:[1，3，5，4，2，0]

**代码#2 : array_form()示例**–2D 置换

```
# Python code explaining
# SymPy.array_form()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.array_form() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - array form : ", a.array_form)
```

**输出:**

> 排列 a–数组形式:[3，2，4，5，0，6，1]