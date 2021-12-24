# Python | SymPy placement .换向器()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-换向器-method/](https://www.geeksforgeeks.org/python-sympy-permutation-commutator-method/)

**arrange .换向器() :换向器()**是一个 sympy Python 库函数，返回分区的换向器。假设‘a’和‘b’是‘C’的一部分，那么 a 和 b 的换向器就是‘C’的同一性**如果 a 和 b 通勤，即 ab == ba。**

> **语法:**
> sympy . combinations .排列.置换.换向器()
> 
> **返回:**分区的
> 换向器

**代码#1:换向器()示例**

```
# Python code explaining
# SymPy.Permutation.commutator()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.commutator() method 

# creating Permutation
a = Permutation([2, 0, 3, 1, 5, 4])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - commutator form : ", a.commutator(b))
print ("Permutation b - commutator form : ", b.commutator(a))
```

**输出:**

> 置换 a–换向形式:置换([3，1，2，5，4，0])
> 置换 b–换向形式:置换([5，1，2，0，4，3])

**代码#2:换向器()示例**–自换向器

```
# Python code explaining
# SymPy.Permutation.commutator()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.commutator() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

# SELF COMMUTATING    
print ("Permutation a - commutator form : ", a.commutator(a))
```

**输出:**

> 置换 a–换向器形式:置换([]，大小=7)