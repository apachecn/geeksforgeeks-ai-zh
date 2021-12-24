# Python 中的 SymPy | arrange . rank _ nonlex()

> 原文:[https://www . geeksforgeeks . org/sympy-置换-rank_nonlex-in-python/](https://www.geeksforgeeks.org/sympy-permutation-rank_nonlex-in-python/)

**arrangement . rank _ nonlex():rank _ nonlex()**是一个 sympy Python 库函数，返回非字典序排列的秩。

> **语法:**sympy . combinations . arranges . arrange . rank _ nonlex()
> 
> **返回:**非辞书排列的秩。

**代码#1 : rank_nonlex()示例**

```
# Python code explaining
# SymPy.Permutation.rank_nonlex()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.rank_nonlex() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - rank_nonlex form : ", a.rank_nonlex())
print ("Permutation b - rank_nonlex form : ", b.rank_nonlex())
```

**输出:**

> 排列 a–秩 _ 非复数形式:13
> 排列 b–秩 _ 非复数形式:72

**代码#2 : rank_nonlex()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.rank_nonlex()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.rank_nonlex() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - rank_nonlex form : ", a.rank_nonlex())
```

**输出:**

> 排列 a–rank _ nonlex 形式:218