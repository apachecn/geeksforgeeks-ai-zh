# Python 中的 SymPy | arrangement . unrank _ trotterjohnson()

> 原文:[https://www . geeksforgeeks . org/sympy-置换-unlank _ trotterjohnson-in-python/](https://www.geeksforgeeks.org/sympy-permutation-unrank_trotterjohnson-in-python/)

**arrangement . unrank _ trotterjohnson():unrank _ trotterjohnson()**是一个 sympy Python 库函数，返回 trotterjohnson 排列 unranking

> **语法:**sympy . combinations . arranges . arrangement . unrank _ trotterjohnson()
> 
> **返回:**特罗特·约翰逊排列解开

**代码# 1:unlank _ trotterjohnson()示例**

```
# Python code explaining
# SymPy.Permutation.unrank_trotterjohnson()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.unrank_trotterjohnson() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

size = 3

rank = 5

print ("Permutation a - unrank_trotterjohnson form : ", a.unrank_trotterjohnson(size, rank))
print ("Permutation b - unrank_trotterjohnson form : ", b.unrank_trotterjohnson(5, rank))
```

**输出:**

> 排列 a–unrank _ trotterjohnson 形式:(2)(0 1)
> 排列 b–unrank _ trotterjohnson 形式:(0 4 2 1)

**代码# 2:unlank _ trotterjohnson()示例**

```
# Python code explaining
# SymPy.Permutation.unrank_trotterjohnson()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.unrank_trotterjohnson() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - unrank_trotterjohnson form : ", a.unrank_trotterjohnson(4, 8))
```

**输出:**

> 排列 a–unrank _ trotterjohnson 形式:(3)(0 2 1)