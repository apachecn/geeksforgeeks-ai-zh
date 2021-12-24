# Python 中的 SymPy | Partition.as_ferrers()

> 原文:[https://www . geesforgeks . org/sympy-partition-as _ ferrers-in-python/](https://www.geeksforgeeks.org/sympy-partition-as_ferrers-in-python/)

**partition . as _ ferrers():as _ ferrers()**是一个 sympy Python 库函数，根据提到的字符返回分区的 ferrer 图。

> **语法:**sympy . combinations . partitions . partition . as _ ferrers(char)
> 
> **返回:**分区的费雷尔图

**代码#1 : as_ferrers()示例**

```py
# Python code explaining
# SymPy.as_ferrers()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import IntegerPartition

# Using from sympy.combinatorics.partitions.Partition.as_ferrers() method 
print(IntegerPartition([5, 2, 5]).as_ferrers())
```

**输出:**

> #####
> #####
> ##

**代码#2 : as_ferrers(char = '*)示例**

```py
# Python code explaining
# SymPy.as_ferrers()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import IntegerPartition

# Using from sympy.combinatorics.partitions.Partition.as_ferrers() method 
print(IntegerPartition([1, 2, 3, 4]).as_ferrers(char = '*'))
```

**输出:**

> * * * *
> * *
> * *
> *