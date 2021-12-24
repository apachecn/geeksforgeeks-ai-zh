# Python | SymPy partition . sort _ key()方法

> 原文:[https://www . geesforgeks . org/python-sympy-partition-sort _ key-method/](https://www.geeksforgeeks.org/python-sympy-partition-sort_key-method/)

**partition . sort _ key():sort _ key()**是一个 sympy Python 库函数，返回可用于字符串的规范键。规范键的这种排序是基于分区的大小和元素，分区与等级的联系被打破。

> **语法:**sympy . combinations . partitions . partition . sort _ key()
> 
> **返回:**可用于字符串的字符键

**代码#1 : sort_key()示例**

```
# Python code explaining
# SymPy.sort_key()

# importing SymPy libraries

from sympy.utilities.iterables import default_sort_key
from sympy.combinatorics.partitions import Partition
from sympy.abc import x

# Using from sympy.combinatorics.partitions.Partition.sort_key() method 
g = Partition([134, 322])
e = Partition(list(range(3)))
k = Partition([44, x])
s = Partition([3, 4])

lst = [s, k, g + 1, k, e]
lst.sort(key = default_sort_key); lst
```

**输出:**

> [{{3，4}}，{{44，x}}，{{44，x}}，{{134}，{322}}，{{0，1，2}}]

**代码#2 : sort_key()示例**

```
# Python code explaining
# SymPy.sort_key()

# importing SymPy libraries

from sympy.utilities.iterables import default_sort_key
from sympy.combinatorics.partitions import Partition
from sympy.abc import x, y

# Using from sympy.combinatorics.partitions.Partition.sort_key() method 

k = Partition([44, x, y])
s = Partition([3, 55, 12, 4])

lst = [k, s]
lst.sort(key = default_sort_key); lst
```

**输出:**

> [{{44，x，y}}，{{3，4，12，55}}]