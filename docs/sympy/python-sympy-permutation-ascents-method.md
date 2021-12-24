# Python | SymPy 排列. ascents()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-ascents-method/](https://www.geeksforgeeks.org/python-sympy-permutation-ascents-method/)

**arrangement . ascents():ascents()**是一个 sympy Python 库函数，返回置换中 ascents 的位置。
上升是 a[i] < a[i+1]所在的元素

> **语法:**sympy . combinations .排列.置换. ascents()
> 
> **返回:**置换中的上升位置

**代码#1:上升()示例**

```py
# Python code explaining
# SymPy.ascents()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.ascents() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - ascents form : ", a.ascents())
print ("Permutation b - ascents form : ", b.ascents())
```

**输出:**

> 排列 a–上升形式:[0，2]
> 排列 b–上升形式:[0，1]

**代码#2 : ascents()示例**–2D 置换

```py
# Python code explaining
# SymPy.ascents()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.ascents() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - ascents form : ", a.ascents())
```

**输出:**

> 排列 a–上升形式:[1，2，4]