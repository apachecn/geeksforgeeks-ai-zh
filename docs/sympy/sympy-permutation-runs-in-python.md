# Python 中的 SymPy | arrange . runs()

> 原文:[https://www . geeksforgeeks . org/sympy-置换-python 中的 runs/](https://www.geeksforgeeks.org/sympy-permutation-runs-in-python/)

**arrange . runs():runs()**是一个 sympy Python 库函数，返回排列的游程。

游程=排列中的升序序列

> **语法:**sympy . combinations .排列.置换. runs()
> 
> **返回:**排列的运行。

**代码#1:运行()示例**

```
# Python code explaining
# SymPy.Permutation.runs()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.runs() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - runs form : ", a.runs())
print ("Permutation b - runs form : ", b.runs())
```

**输出:**

> 排列 a–游程形式:[[2，3]，[0，1]]
> 排列 b–游程形式:[[1，3，5]，[4]，[2]，[0]]

**代码#2:运行()示例**

```
# Python code explaining
# SymPy.Permutation.runs()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.runs() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - runs form : ", a.runs())
```

**输出:**

> 排列 a–运行形式:[[3]，[2，4，5]，[0，6]，[1]]