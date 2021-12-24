# Python 中的 SymPy | Partition .共轭()

> 原文:[https://www . geesforgeks . org/sympy-partition-共轭 in-python/](https://www.geeksforgeeks.org/sympy-partition-conjugate-in-python/)

**partition . concurrent():concurrent()**是一个 sympy Python 库函数，返回参数化分区的共轭分区。

> **语法:**sympy . combinations . partitions . partition .共轭()
> 
> **返回:**共轭配分

**代码#1:共轭()示例**

```
# Python code explaining
# SymPy.conjugate()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import IntegerPartition

# Using from sympy.combinatorics.partitions.Partition.conjugate() method 
p = IntegerPartition([312, 14, 23])
print ('Conjugate : ', p.conjugate)
```

**输出:**

> 共轭:[3，3，3，3，3，3，3，3，3，3，3，2，2，2，2，2，2，2，2，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1，1 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1]

**代码#2:共轭()示例–显示值错误。**

```
# Python code explaining
# SymPy.conjugate()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import IntegerPartition

# Using from sympy.combinatorics.partitions.Partition.conjugate() method 

# Only positive elements are required 
# so this will generate error
p = IntegerPartition([312, 14, -10, 23, -1])
print ('Conjugate : ', p.conjugate)
```

**输出:**

> 值错误:总和必须都是正数。