# 症状|分区。Python 中的 RGS_enum()

> 原文:[https://www . geesforgeks . org/sympy-partition-rgs _ enum-in-python/](https://www.geeksforgeeks.org/sympy-partition-rgs_enum-in-python/)

**分区。RGS_enum() : RGS_enum()** 是一个 sympy Python 库函数，它计算**受限增长字符串的总数(其中 a[i]是元素 I 出现的块的字符串)**，这对于大小为 n 的超集是可能的。

**限制生长字符串–**字符串，其中每个字符，一个 <sub>i</sub> 产生对应元素所属的块(B <sub>i</sub> )。

> **语法:**sympy . combinations . partitions . partition . rgs _ enum()
> 
> **返回:**受限生长字符串的总数，可能是 n 大小的超集。

**代码#1 : RGS_enum()示例**

```
# Python code explaining
# SymPy.RGS_enum()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import RGS_enum

# Using from sympy.combinatorics.partitions.Partition.RGS_enum() method 
p = RGS_enum(4)

q = RGS_enum(9)

print ("no. of strings possible for size  4: ", p)
print ("no. of strings possible for size  9: ", q)
```

**输出:**

> 尺寸为 4: 15 的可能弦数
> 尺寸为 9: 203 的可能弦数

**代码#2 : RGS_enum()示例**

```
# Python code explaining
# SymPy.RGS_enum()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import RGS_enum

# Using from sympy.combinatorics.partitions.Partition.RGS_enum() method 
p = RGS_enum(20)

q = RGS_enum(-1)

print ("no. of strings possible for size  20 ", p)
print ("no. of strings possible for size  -1: ", q)
```

**输出:**

> 大小为 20 的可能字符串数 51724158235372
> 大小为-1: 0 的可能字符串数