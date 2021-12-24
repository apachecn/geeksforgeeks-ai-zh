# Python 中的 SymPy | arrangement . is _ Identity()

> 原文:[https://www . geesforgeks . org/sympy-arrange-is _ identity-in-python/](https://www.geeksforgeeks.org/sympy-permutation-is_identity-in-python/)

 **arrangement . is _ Identity():is _ Identity()**是一个 sympy Python 库函数，用于检查 arrange 是否是一个身份置换。

> **语法:**sympy . combinations .排列.置换. is_Identity()
> 
> **返回:**true–如果他置换是一个身份置换；否则为假

**代码#1 : is_Identity()示例**

```
# Python code explaining
# SymPy.Permutation.is_Identity()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.is_Identity() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - is_Identity form : ", a.is_Identity)
print ("Permutation b - is_Identity form : ", b.is_Identity)
```

**输出:**

> 排列 a–is _ Identity 形式:假
> 排列 b–is _ Identity 形式:假

**代码#2 : is_Identity()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.is_Identity()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.is_Identity() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - is_Identity form : ", a.is_Identity)
```

**输出:**

> 排列 a–is _ Identity 形式:假