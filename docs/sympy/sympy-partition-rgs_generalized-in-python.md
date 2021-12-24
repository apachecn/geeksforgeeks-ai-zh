# 症状|分区。Python 中的 RGS _ generalized()

> 原文:[https://www . geesforgeks . org/sympy-partition-rgs _ generalized-in-python/](https://www.geeksforgeeks.org/sympy-partition-rgs_generalized-in-python/)

**分区。RGS _ generalized():RGS _ generalized()**是一个 sympy Python 库函数，它计算 **m + 1 个广义无限制增长字符串(其中 a[i]是元素 I 出现的块的字符串)**，然后将其作为矩阵中的行返回。

受限增长字符串–每个字符中的一个 <sub>i</sub> 导致对应元素所属的块(B <sub>i</sub> )的字符串。

> **语法:**sympy . combinations . partitions . partition . rgs _ generated()
> 
> **返回:**广义无限制生长字符串作为矩阵的行。

**代码# 1:RGS _ generated()示例**

```
]

# Python code explaining
# SymPy.RGS_generalized()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import RGS_generalized

# Using from sympy.combinatorics.partitions.Partition.RGS_generalized() method 
p = RGS_generalized(3)

print ("Row of Matrix : \n", p)
```

**输出:**

> 矩阵行:
> 矩阵([[1，1，1，1]，[1，2，3，0]，[2，5，0，0]，[5，0，0，0]])

**代码# 2:RGS _ generated()示例**

```
]

# Python code explaining
# SymPy.RGS_generalized()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import RGS_generalized

# Using from sympy.combinatorics.partitions.Partition.RGS_generalized() method 
p = RGS_generalized(-1)

print ("Row of Matrix : \n", p)
```

**输出:**

> 矩阵行:
> 矩阵(0，0，[])