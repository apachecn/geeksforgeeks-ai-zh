# Python 中的 SymPy | arrangement . next _ trotterjohnson()

> 原文:[https://www . geeksforgeeks . org/sympy-置换-next _ trotterjohnson-in-python/](https://www.geeksforgeeks.org/sympy-permutation-next_trotterjohnson-in-python/)

**arrangement . next _ trotterjohnson():next _ trotterjohnson()**是一个 sympy Python 库函数，返回 Trotter-Johnson 顺序的下一个排列。如果 self 是最后一个置换，则返回 None。

> **语法:**sympy . combinations . arranges . arrangement . next _ trotterjohnson()
> 
> **返回:**特罗特-约翰逊顺序的下一个排列

**代码#1 : next_trotterjohnson()示例**

```
# Python code explaining
# SymPy.Permutation.next_trotterjohnson()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.next_trotterjohnson() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - next_trotterjohnson form : ", a.next_trotterjohnson())
print ("Permutation b - next_trotterjohnson form : ", b.next_trotterjohnson())
```

**输出:**

> 排列 a–next _ trotterjohnson 形式:(0 3 1 2)
> 排列 b–next _ trotterjohnson 形式:(0 1 5)(2 3 4)

**代码#2 : next_trotterjohnson()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.next_trotterjohnson()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.next_trotterjohnson() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - next_trotterjohnson form : ", a.next_trotterjohnson())
```

**输出:**

> 排列 a–next _ trotterjohnson 形式:(6)(0 3 5 1 2 4)