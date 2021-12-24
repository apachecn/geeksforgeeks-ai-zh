# Python | SymPy 组合学. prev_lex()方法

> 原文:[https://www . geesforgeks . org/python-sympy-combinarics-prev _ lex-method/](https://www.geeksforgeeks.org/python-sympy-combinatorics-prev_lex-method/)

借助`**sympy.combinatorics.partitions.IntegerPartition().prev_lex()**`方法，我们可以利用`sympy.combinatorics.partitions.IntegerPartition().prev_lex()`方法得到整数 n 在词法顺序上的上一次划分。

> **语法:** `sympy.combinatorics.partitions.IntegerPartition().prev_lex()`
> **返回:**返回整数 n 的前一个分区的词法值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.combinatorics.partitions.IntegerPartition().prev_lex()`方法，我们能够得到整数 n 的前一个分区的词法值。

```py
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import IntegerPartition
from sympy import *

# Using sympy.combinatorics.partitions.IntegerPartition().prev_lex() method
gfg = IntegerPartition([1, 2, 3])

print(gfg.prev_lex())
```

**输出:**

> [3, 1, 1, 1]

**例 2 :**

```py
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import IntegerPartition
from sympy import *

# Using sympy.combinatorics.partitions.IntegerPartition().prev_lex() method
gfg = IntegerPartition([1, 2, 3, 4, 3, 2, 1])

print(gfg.prev_lex())
```

**输出:**

> [4, 3, 3, 2, 1, 1, 1, 1]