# Python | SymPy placement . cycle _ structure()方法

> 原文:[https://www . geesforgeks . org/python-sympy-置换-cycle_structure-method/](https://www.geeksforgeeks.org/python-sympy-permutation-cycle_structure-method/)

**replacement . cycle _ structure():cycle _ structure()**是一个 sympy Python 库函数，它将置换的循环结构作为字典返回，这将指示每个循环长度的多重性。

> **语法:**
> sympy . combinations .排列.置换. cycle_structure()
> 
> **返回:**
> 循环结构的排列作为字典

**代码#1 : cycle_structure()示例**

```py
# Python code explaining
# SymPy.Permutation.cycle_structure()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.cycle_structure() method 

# creating Permutation
a = Permutation([2, 0, 3, 1, 5, 4])

b = Permutation([3, 1, 2, 5, 4, 0])

print ("Permutation a - cycle_structure form : ", a.cycle_structure)
print ("Permutation b - cycle_structure form : ", b.cycle_structure)
```

**输出:**

> 置换 a–cycle _ structure 形式:{2: 1，4: 1}
> 置换 b–cycle _ structure 形式:{1: 3，3: 1}

**代码#2 : cycle_structure()示例**–2D 置换

```py
# Python code explaining
# SymPy.Permutation.cycle_structure()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from 
# sympy.combinatorics.permutations.Permutation.cycle_structure() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

# SELF COMMUTATING    
print ("Permutation a - cycle_structure form : ", a.cycle_structure)
```

**输出:**

> 排列 a–cycle _ structure 形式:{7: 1}