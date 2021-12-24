# Python 中的 SymPy | arrangement . next _ nonlex()

> 原文:[https://www . geesforgeks . org/sympy-置换-next_nonlex-in-python/](https://www.geeksforgeeks.org/sympy-permutation-next_nonlex-in-python/)

**arrangement . next _ nonlex():next _ nonlex()**是一个 sympy Python 库函数，它以非词典顺序返回下一个排列，如果 self 是非词典顺序的最后一个排列，则返回 None。

> **语法:**sympy . combinations .排列.置换. next_nonlex()
> 
> **返回:**非词典顺序的下一个排列

**代码#1 : next_nonlex()示例**

```py
# Python code explaining
# SymPy.Permutation.next_nonlex()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.next_nonlex() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - next_nonlex form : ", a.next_nonlex())
print ("Permutation b - next_nonlex form : ", b.next_nonlex())
```

**输出:**

> 排列 a–next _ non lex 形式:(0 3 2)
> 排列 b–next _ non lex 形式:(0 5 1 3 4 2)

**代码#2 : next_nonlex()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.next_nonlex()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.next_nonlex() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - next_nonlex form : ", a.next_nonlex())
```

**输出:**

> 排列 a–next _ nonlex 形式:(0 3 5 1 6 2 4)