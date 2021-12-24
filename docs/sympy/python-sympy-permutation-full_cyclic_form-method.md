# Python | SymPy placement . full _ cyclic _ form()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-full_cyclic_form-method/](https://www.geeksforgeeks.org/python-sympy-permutation-full_cyclic_form-method/)

**replacement . full _ cyclic _ form():full _ cyclic _ form()**是一个 sympy Python 库函数，通过包含单线态以循环形式返回置换。

> **语法:**
> sympy . combinations .排列.置换. full_cyclic_form()
> 
> **返回:**
> 循环形式的置换

**代码#1 : full_cyclic_form()示例**

```py
# Python code explaining
# SymPy.Permutation.full_cyclic_form()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.full_cyclic_form() method 

# creating Permutation
a = Permutation([2, 0, 3, 1, 5, 4])

b = Permutation([3, 1, 2, 5, 4, 0])

print ("Permutation a - full_cyclic_form form : ", a.full_cyclic_form)
print ("Permutation b - full_cyclic_form form : ", b.full_cyclic_form)
```

**输出:**

> 置换 a–完全 _ 循环 _ 形式形式:[[0，2，3，1]，[4，5]]
> 置换 b–完全 _ 循环 _ 形式形式:[[0，3，5]，[1]，[2]，[4]]

**代码#2:全循环形式()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.full_cyclic_form()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.full_cyclic_form() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - full_cyclic_form form : ", a.full_cyclic_form)
```

**输出:**

> 置换 a–full _ cyclic _ form 形式:[[0，3，5，6，1，2，4]]