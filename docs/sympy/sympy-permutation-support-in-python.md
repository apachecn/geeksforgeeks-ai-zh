# Python 中的 SymPy | arrange . support()

> 原文:[https://www . geesforgeks . org/sympy-置换-python 中的支持/](https://www.geeksforgeeks.org/sympy-permutation-support-in-python/)

**replacement . support():support()**是一个 sympy Python 库函数，返回 replacement 中的元素，P，为此 P[i]！= i。

> **语法:**sympy . combinations .排列.置换. support()
> 
> **返回:**排列中的元素，P，为哪个 P[i]！= i。

**代码#1:支持()示例**

```py
# Python code explaining
# SymPy.Permutation.support()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.support() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - support form : ", a.support())
print ("Permutation b - support form : ", b.support())
```

**输出:**

> 排列 a–支持形式:[0，1，2，3]
> 排列 b–支持形式:[0，1，2，3，4，5]

**代码#2:支持()示例**

```py
# Python code explaining
# SymPy.Permutation.support()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.support() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - support form : ", a.support())
```

**输出:**

> 排列 a–支持形式:[0，1，2，3，4，5，6]