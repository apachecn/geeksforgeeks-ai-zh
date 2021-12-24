# Python 中的 SymPy | arrangement . is _ Singleton()

> 原文:[https://www . geesforgeks . org/sympy-arrange-is _ singleton-in-python/](https://www.geeksforgeeks.org/sympy-permutation-is_singleton-in-python/)

**arrangement . is _ Singleton():is _ Singleton()**是一个 sympy Python 库函数，检查置换是否只包含一个单个元素。

> **语法:**sympy . combinations . arranges . arrangement . is _ Singleton()
> 
> **返回:**true–如果置换只有一个元素；否则为假

**代码#1 : is_Singleton()示例**

```py
# Python code explaining
# SymPy.Permutation.is_Singleton()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.is_Singleton() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([0])

print ("Permutation a - is_Singleton form : ", a.is_Singleton)
print ("Permutation b - is_Singleton form : ", b.is_Singleton)
```

**输出:**

> 排列 a–is _ Singleton 形式:假
> 排列 b–is _ Singleton 形式:真

**代码#2 : is_Singleton()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.is_Singleton()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.is_Singleton() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - is_Singleton form : ", a.is_Singleton)
```

**输出:**

> 排列 a–is _ Singleton 形式:假