# Python 中的 SymPy | arrangement . unlank _ nonlex()

> 原文:[https://www . geesforgeks . org/sympy-置换-unlank _ nonlex-in-python/](https://www.geeksforgeeks.org/sympy-permutation-unrank_nonlex-in-python/)

**arrangement . unlank _ nonlex():unlank _ nonlex()**是一个 sympy Python 库函数，是一个不尊重字典顺序的线性时间解开算法。

> **语法:**sympy . combinations . arranges . arrangement . unlank _ nonlex()
> 
> **返回:**线性时间解开。

**代码# 1:unlank _ nonlex()示例**

```py
# Python code explaining
# SymPy.Permutation.unrank_nonlex()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.unrank_nonlex() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - unrank_nonlex form : ", a.unrank_nonlex(2, 5))
print ("Permutation b - unrank_nonlex form : ", b.unrank_nonlex(1, 6))
```

**输出:**

> 排列 a–unlank _ nonlex 形式:(1)
> 排列 b–unlank _ nonlex 形式:(0)

**代码# 2:unlank _ nonlex()示例**

```py
# Python code explaining
# SymPy.Permutation.unrank_nonlex()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.unrank_nonlex() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - unrank_nonlex form : ", a.unrank_nonlex(2, 8))
```

**输出:**

> 排列 a–unlank _ nonlex 形式:(0 1)