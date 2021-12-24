# Python | SymPy 组合学. random_integer_partition()方法

> 原文:[https://www . geesforgeks . org/python-sympy-combinations-random _ integer _ partition-method/](https://www.geeksforgeeks.org/python-sympy-combinatorics-random_integer_partition-method/)

借助`**sympy.combinatorics.partitions.random_integer_partition()**`方法，我们可以用`sympy.combinatorics.partitions.random_integer_partition()`方法得到倒排排序列表形式的 n 的随机划分。

> **语法:** `sympy.combinatorics.partitions.random_integer_partition(n)`
> **返回:**返回 n 个分区整数的反向排序列表。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.combinatorics.partitions.random_integer_partition()`方法，我们能够获得整数随机划分的反向排序列表。

```py
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import random_integer_partition
from sympy import *

# Using sympy.combinatorics.partitions.random_integer_partition() method
gfg = random_integer_partition(50)

print(gfg)
```

**输出:**

> [22, 22, 5, 1]

**例 2 :**

```py
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import random_integer_partition
from sympy import *

# Using sympy.combinatorics.partitions.random_integer_partition() method
gfg = random_integer_partition(25)

print(gfg)
```

**输出:**

> [12, 11, 1, 1]