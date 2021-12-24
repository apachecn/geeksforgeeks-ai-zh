# Python | sympy IntegerPartition()方法

> 原文:[https://www . geesforgeks . org/python-sympy-integer partition-method/](https://www.geeksforgeeks.org/python-sympy-integerpartition-method/)

借助`**sympy.combinatorics.partitions.IntegerPartition()**`方法，我们可以得到子阵列中的元素，这些元素在`sympy.combinatorics.Partition().rank`方法中作为参数传递。

> **语法:** `sympy.combinatorics.partitions.IntegerPartition()`
> **返回:**返回整数值的分区。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.combinatorics.partitions.IntegerPartition()`方法，我们能够得到整数值的划分。

```
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import IntegerPartition
from sympy import *

# Using sympy.combinatorics.partitions.IntegerPartition() method
gfg = IntegerPartition([1] + [2, 3])

print(gfg)
```

**输出:**

> [3, 2, 1]

**例 2 :**

```
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import IntegerPartition
from sympy import *

# Using sympy.combinatorics.partitions.IntegerPartition() method
gfg = IntegerPartition([1] + [2, 3] + [4] + [5])

print(gfg)
```

**输出:**

> [5, 4, 3, 2, 1]