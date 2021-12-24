# Python 中的 SymPy | arrangement . unlank _ lex()

> 原文:[https://www . geesforgeks . org/sympy-置换-unlank _ lex-in-python/](https://www.geeksforgeeks.org/sympy-permutation-unrank_lex-in-python/)

 **arrangement . unlank _ lex():unlank _ lex()**是一个 sympy Python 库函数，返回字典排列 unranking。

> **语法:**sympy . combinations . arranges . arrangement . unlank _ lex()
> 
> **返回:**字典排列解开

**代码# 1:unlank _ lex()示例**

```
# Python code explaining
# SymPy.Permutation.unrank_lex()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.unrank_lex() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

size = 2
rank = 5

print ("Permutation a - unrank_lex form : ", a.unrank_lex(size, rank))
print ("Permutation b - unrank_lex form : ", b.unrank_lex(size, 2))
```

**输出:**

> 排列 a–unlank _ lex 形式:(0 1)
> 排列 b–unlank _ lex 形式:(1)

**代码# 2:unlank _ lex()示例**

```
# Python code explaining
# SymPy.Permutation.unrank_lex()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.unrank_lex() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - unrank_lex form : ", a.unrank_lex(5, 2))
```

**输出:**

> 排列 a–unlank _ lex 形式:(4)(2 3)