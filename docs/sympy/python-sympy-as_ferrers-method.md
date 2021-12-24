# Python | sympy as_ferrers()方法

> 原文:[https://www . geesforgeks . org/python-sympy-as _ ferrers-method/](https://www.geeksforgeeks.org/python-sympy-as_ferrers-method/)

借助`**sympy.combinatorics.IntegerPartition().as_ferrers()**`方法，我们可以用`sympy.combinatorics.IntegerPartition().as_ferrers()`方法得到分区值的费雷尔图。

> **语法:** `sympy.combinatorics.IntegerPartition().as_ferrers()`
> 
> **返回:**返回费雷尔图。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.combinatorics.IntegerPartition().as_ferrers()`方法，我们能够获得费雷尔图。

```py
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import IntegerPartition
from sympy import *

# Using sympy.combinatorics.partitions.IntegerPartition().as_ferrers() method
gfg = IntegerPartition([1] + [2, 3]).as_ferrers()

print(gfg)
```

**输出:**

> ###
> ##
> #

**例 2 :**

```py
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import IntegerPartition
from sympy import *

# Using sympy.combinatorics.partitions.IntegerPartition().as_ferrers() method
gfg = IntegerPartition([1] + [2, 3] + [4] + [5]).as_ferrers(char ='{content}apos;)

print(gfg)
```

**输出:**

> $ $ $
> $
> $
> $
> $