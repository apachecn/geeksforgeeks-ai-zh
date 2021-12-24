# 症状|分区。Python 中的 RGS_rank()

> 原文:[https://www . geesforgeks . org/sympy-partition-rgs _ rank-in-python/](https://www.geeksforgeeks.org/sympy-partition-rgs_rank-in-python/)

**分区。RGS_rank(rank，n) : RGS_rank()** 是一个 sympy Python 库函数，给出了一个**受限增长字符串(其中 a[i]是元素 I 所在的块的字符串)**的排名。

**限制生长字符串–**字符串，其中每个字符，一个 <sub>i</sub> 产生对应元素所属的块(B <sub>i</sub> )。

> **语法:**sympy . combinations . partitions . partition . rgs _ rank()
> 
> **返回:**限制生长字符串的等级。

**代码#1 : RGS_rank()示例**

```
# Python code explaining
# SymPy.RGS_rank()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import RGS_rank

# Using from sympy.combinatorics.partitions.Partition.RGS_rank() method 
p = RGS_rank([0, 0, 1, 1, 2])

print ("rank for restricted growth string : \n", p)
```

**输出:**

> 受限生长字符串的等级:
> 10

**代码#2 : RGS_rank()示例**

```
# Python code explaining
# SymPy.RGS_rank()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import RGS_rank

# Using from sympy.combinatorics.partitions.Partition.RGS_rank() method 
p = RGS_rank( [0, 0, 0, 0, 0, 1, 1, 1, 0, 1])

print ("rank for restricted growth string : \n", p)
```

**输出:**

> 受限生长字符串的等级:
> 100