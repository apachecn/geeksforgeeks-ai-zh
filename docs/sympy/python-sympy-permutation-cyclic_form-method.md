# Python | SymPy placement . cyclic _ form()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-cyclic_form-method/](https://www.geeksforgeeks.org/python-sympy-permutation-cyclic_form-method/)

**replacement . cyclic _ form():cyclic _ form()**是一个 sympy Python 库函数，通过省略单线态，从规范符号返回循环符号。

> **语法:**
> 符号组合学.排列.置换.循环形式()
> 
> **从规范符号返回:**
> 循环符号

**代码#1:循环形式()示例**

```
# Python code explaining
# SymPy.Permutation.cyclic_form()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.cyclic_form() method 

# creating Permutation
a = Permutation([2, 0, 3, 1, 5, 4])

b = Permutation([3, 1, 2, 5, 4, 0])

print ("Permutation a - cyclic_form form : ", a.cyclic_form)
print ("Permutation b - cyclic_form form : ", b.cyclic_form)
```

**输出:**

> 排列 a–循环形式:[[0，2，3，1]，[4，5]]
> 排列 b–循环形式:[[0，3，5]]

**代码#2:循环形式()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.cyclic_form()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.cyclic_form() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

# SELF COMMUTATING    
print ("Permutation a - cyclic_form form : ", a.cyclic_form)
```

**输出:**

> 置换 a–循环形式形式:[[0，3，5，6，1，2，4]]