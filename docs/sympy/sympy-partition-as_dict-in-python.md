# Python 中的 SymPy | Partition.as_dict()

> 原文:[https://www . geesforgeks . org/sympy-partition-as _ dict-in-python/](https://www.geeksforgeeks.org/sympy-partition-as_dict-in-python/)

**partition . as _ dict():as _ dict()**是一个 sympy Python 库函数，将分区作为字典返回。在本字典中，键是分区整数。这些值是该整数的倍数。

> **语法:**sympy . combinations . partitions . partition . as _ dict()
> 
> **返回:**分区为字典

**代码#1 : as_dict()示例**

```
# Python code explaining
# SymPy.as_dict()

# importing SymPy libraries

from sympy.utilities.iterables import default_sort_key
from sympy.combinatorics.partitions import Partition
from sympy.abc import x, y
from sympy.combinatorics.partitions import IntegerPartition

# Using from sympy.combinatorics.partitions.Partition.as_dict() method 
IntegerPartition([11]*3 + [342] + [13]*4).as_dict()
```

**输出:**

> {11: 3, 13: 4, 342: 1}

**代码#2 : as_dict()示例**

```
# Python code explaining
# SymPy.as_dict()

# importing SymPy libraries

from sympy.utilities.iterables import default_sort_key
from sympy.combinatorics.partitions import Partition
from sympy.abc import x, y
from sympy.combinatorics.partitions import IntegerPartition

# Using from sympy.combinatorics.partitions.Partition.as_dict() method 
IntegerPartition([100]*100 + [342]*10 + [13] + [2232]).as_dict()
```

**输出:**

> {13: 1, 100: 100, 342: 10, 2232: 1}