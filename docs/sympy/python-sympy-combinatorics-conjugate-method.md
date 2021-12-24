# Python | SymPy 组合学.共轭()方法

> 原文:[https://www . geesforgeks . org/python-sympy-combinations-共轭-method/](https://www.geeksforgeeks.org/python-sympy-combinatorics-conjugate-method/)

借助`**sympy.combinatorics.partitions.IntegerPartition().conjugate**`方法，我们可以得到在`sympy.combinatorics.partitions.IntegerPartition()`方法中作为参数传递的整数数组的共轭值。

> **语法:** `sympy.combinatorics.partitions.IntegerPartition().conjugate`
> **返回:**返回整型数组的共轭值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.combinatorics.partitions.IntegerPartition().conjugate`方法，我们能够获得作为参数传递的数组的共轭值。

```
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import IntegerPartition
from sympy import *

# Using sympy.combinatorics.partitions.IntegerPartition().conjugate method
gfg = IntegerPartition([1, 2, 3])

print(gfg.conjugate)
```

**输出:**

> [3, 2, 1]

**例 2 :**

```
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import IntegerPartition
from sympy import *

# Using sympy.combinatorics.partitions.IntegerPartition().conjugate method
gfg = IntegerPartition([1, 2, 3, 4, 3, 2, 1])

print(gfg.conjugate)
```

**输出:**

> [7, 5, 3, 1]