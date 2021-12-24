# Python 中的 SymPy | arrange . is _ Empty()

> 原文:[https://www . geeksforgeeks . org/sympy-arrange-is _ empty-in-python/](https://www.geeksforgeeks.org/sympy-permutation-is_empty-in-python/)

**replacement . is _ Empty():is _ Empty()**是一个 sympy Python 库函数，检查置换是否是零元素的集合。

> **语法:**sympy . combinations . arranges . arrange . is _ Empty()
> 
> **返回:** true:如果为空；否则为假

**代码#1 : is_Empty()示例**

```py
# Python code explaining
# SymPy.Permutation.is_Empty()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.is_Empty() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - is_Empty form : ", a.is_Empty)
print ("Permutation b - is_Empty form : ", b.is_Empty)
```

**输出:**

> 排列 a–is _ 空形式:假
> 排列 b–is _ 空形式:假

**代码#2 : is_Empty()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.is_Empty()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.is_Empty() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - is_Empty form : ", a.is_Empty)
```

**输出:**

> 排列 a–is _ 空形式:假