# Python | SymPy placement .通勤 _with()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-通勤 _with-method/](https://www.geeksforgeeks.org/python-sympy-permutation-commutes_with-method/)

 **replacement .通勤 _with():通勤 _with()** 是一个 sympy Python 库函数，检查两个置换是否在通勤。假设‘a’和‘b’是‘C’的一部分，那么 a 和 b 的换向器就是‘C’的同一性**if a 和 b 的通勤，即 ab == ba。**

> **语法:**
> sympy . combinations . arranges . replacement .通勤 _with()
> 
> **返回:**
> 检查两个排列是否在交换

**代码#1:用()通勤 _ 示例**

```
# Python code explaining
# SymPy.Permutation.commutes_with()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.commutes_with() method 

# creating Permutation
a = Permutation([2, 0, 3, 1, 5, 4])

b = Permutation([3, 1, 2, 5, 4, 0])

print ("Permutation a - commutes_with form : ", a.commutes_with(b))
print ("Permutation b - commutes_with form : ", b.commutes_with(a))
```

**输出:**

> 排列 a–以形式通勤 _ 假
> 排列 b–以形式通勤 _ 假

**代码#2:用()通勤 _ 示例**–自换向器

```
# Python code explaining
# SymPy.Permutation.commutes_with()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.commutes_with() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

# SELF COMMUTATING    
print ("Permutation a - commutes_with form : ", a.commutes_with(a))
```

**输出:**

> 置换 a–用形式通勤 _ 真