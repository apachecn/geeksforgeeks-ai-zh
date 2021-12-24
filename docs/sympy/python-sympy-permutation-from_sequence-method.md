# Python | SymPy placement . from _ sequence()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-from_sequence-method/](https://www.geeksforgeeks.org/python-sympy-permutation-from_sequence-method/)

**replacement . from _ sequence():from _ sequence()**是一个 sympy Python 库函数，返回从“I”的排序元素中获取“I”所需的置换。如果需要任何自定义字符串，也可以将“key”作为参数传递。

> **语法:**
> sympy . combinations .排列.置换. from_sequence()
> 
> **返回:**
> 返回从“I”的排序元素中获得“I”所需的排列

**代码#1 : from_sequence()示例**

```py
# Python code explaining
# SymPy.from_sequence()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.from_sequence() method 

# creating vectors
a = [1, 0, 0, 0]

b = [6, 5, 4, 3, 0, 0 ]

# inversion forms
print ("vector a - from_sequence form : \n", Permutation.from_sequence(a))
print ("vector b - from_sequence form : \n", Permutation.from_sequence(b))
```

**输出:**

> 向量 a–from _ sequence 形式:
> 置换([3，0，1，2])
> 
> 向量 b–from _ sequence 形式:
> 置换([5，4，3，2，0，1])

**代码#2 : from_sequence()示例**–使用字符串和键

```py
# Python code explaining
# SymPy.from_sequence()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.from_sequence() method 

# creating vector
a = [2, 3, 1, 0]

# inverted vector of a
print ("vector a - from_sequence form : ", 
       Permutation.from_sequence(a))

# length = 5, so permutation as per that.
print ("\nstring - from_sequence form : ", 
       Permutation.from_sequence('GEEKS'))

# length = 5, so permutation as per that.
# defining a key
print ("\nstring - from_sequence form : ", 
       Permutation.from_sequence('GEEKS', key = lambda x: x.lower()))
```

**输出:**

> 向量 a–from _ 序列形式:置换([2，3，1，0])
> 
> 字符串–from _ sequence 形式:置换([2，0，1，3，4])
> 
> 字符串–from _ sequence 形式:置换([2，0，1，3，4])