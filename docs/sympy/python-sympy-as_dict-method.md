# Python | sympy as_dict()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-as_dict-method/](https://www.geeksforgeeks.org/python-sympy-as_dict-method/)

借助`**sympy.combinatorics.IntegerPartition().as_dict()**`方法，我们可以利用`sympy.combinatorics.IntegerPartition().as_dict()`方法从子阵中获得整数元素的字典以及它的系数值。

> **语法:** `sympy.combinatorics.IntegerPartition().as_dict()`
> **返回:**返回包含元素及其系数值的字典。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.combinatorics.IntegerPartition().as_dict()`方法，我们能够获得带有其系数值的整数值字典。

```py
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import IntegerPartition
from sympy import *

# Using sympy.combinatorics.partitions.IntegerPartition().as_dict() method
gfg = IntegerPartition([1] + 3 * [2, 3]).as_dict()

print(gfg)
```

**输出:**

> {3: 3, 2: 3, 1: 1}

**例 2 :**

```py
# import sympy and IntegerPartition
from sympy.combinatorics.partitions import IntegerPartition
from sympy import *

# Using sympy.combinatorics.partitions.IntegerPartition().as_dict() method
gfg = IntegerPartition([1] + 2 * [2, 3] + 4 * [4] + 5 * [5]).as_dict()

print(gfg)
```

**输出:**

> {5: 5, 4: 4, 3: 2, 2: 2, 1: 1}