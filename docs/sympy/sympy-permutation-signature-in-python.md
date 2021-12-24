# Python 中的 SymPy | Permutation.signature()

> 原文:[https://www . geesforgeks . org/sympy-置换-python 中的签名/](https://www.geeksforgeeks.org/sympy-permutation-signature-in-python/)

**arrangement . signature():signature()**是一个 sympy Python 库函数，它返回将置换的元素按规范顺序放置所需的置换的签名。
**签名= (-1)^ <倒排数量>**

> **语法:**sympy . combinations .排列.置换. signature()
> 
> **返回:**排列的签名。

**代码#1:签名()示例**

```py
# Python code explaining
# SymPy.Permutation.signature()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.signature() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - signature form : ", a.signature())
print ("Permutation b - signature form : ", b.signature())
```

**输出:**

> 排列 a–签名形式:1
> 排列 b–签名形式:-1

**代码#2:签名()示例**

```py
# Python code explaining
# SymPy.Permutation.signature()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.signature() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - signature form : ", a.signature())
```

**输出:**

> 排列 a–签名形式:1