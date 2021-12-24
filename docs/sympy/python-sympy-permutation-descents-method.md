# Python | SymPy placement . descents()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-descents-method/](https://www.geeksforgeeks.org/python-sympy-permutation-descents-method/)

**置换. descents() : descents()** 是一个 sympy Python 库函数，返回置换中 descents 的位置。下降是 **a[i] > a[i+1]** 的元素

> **语法:**sympy . combinations .排列.置换. descents()
> 
> **返回:**下降在排列中的位置

**代码#1:下降()示例**

```py
# Python code explaining
# SymPy.descents()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.descents() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - descents form : ", a.descents())
print ("Permutation b - descents form : ", b.descents())
```

**输出:**

> 排列 a–下降形式:[1]
> 排列 b–下降形式:[2，3，4]

**代码#2:下降()示例**–2D 排列

```py
# Python code explaining
# SymPy.descents()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.descents() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - descents form : ", a.descents())
```

**输出:**

> 排列 a–下降形式:[0，3，5]