# Python | SymPy placement . atoms()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-atoms-method/](https://www.geeksforgeeks.org/python-sympy-permutation-atoms-method/)

**置换. atoms() : atoms()** 是一个 sympy Python 库函数，返回置换中存在的所有元素。

> **语法:**组合学.排列.排列.原子()
> 
> **返回:**参数化排列的元素。

**代码#1:原子()示例**

```py
# Python code explaining
# SymPy.Permutation.atoms()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.atoms() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - atoms form : ", a.atoms())
print ("Permutation b - atoms form : ", b.atoms())
```

**输出:**

> 排列 a–原子形式:{0，1，2，3}
> 排列 b–原子形式:{0，1，2，3，4，5}

**代码#2:原子()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.atoms()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.atoms() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - atoms form : ", a.atoms())
```

**输出:**

> 排列 a–上升形式:[1，2，4]