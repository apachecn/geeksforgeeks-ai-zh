# Python | SymPy 置换. cycles()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-循环-方法/](https://www.geeksforgeeks.org/python-sympy-permutation-cycles-method/)

**置换. cycles() : cycles()** 是一个 sympy Python 库函数，返回置换中存在的循环数。这也包括单例。

> **语法:**
> 组合学.排列.置换.循环()
> 
> **返回:**
> 排列中出现的循环数

**代码#1:周期()示例**

```
# Python code explaining
# SymPy.Permutation.cycles()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.cycles() method 

# creating Permutation
a = Permutation([2, 0, 3, 1, 5, 4])

b = Permutation([3, 1, 2, 5, 4, 0])

print ("Permutation a - cycles form : ", a.cycles)
print ("Permutation b - cycles form : ", b.cycles)
```

**输出:**

> 置换 a–循环形式:2
> 置换 b–循环形式:4

**代码#2:循环()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.cycles()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.cycles() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

# SELF COMMUTATING    
print ("Permutation a - cycles form : ", a.cycles)
```

**输出:**

> 置换 a–循环形式:1