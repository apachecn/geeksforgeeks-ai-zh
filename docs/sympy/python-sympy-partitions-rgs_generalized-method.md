# Python | sympy 分区。RGS _ 广义()方法

> 原文:[https://www . geesforgeks . org/python-sympy-partitions-rgs _ generalized-method/](https://www.geeksforgeeks.org/python-sympy-partitions-rgs_generalized-method/)

借助`**sympy.combinatorics.partitions.RGS_generalized()**`方法，我们可以得到 m+1 个无限制生长字符串，并使用`sympy.combinatorics.partitions.RGS_generalized()`方法返回一个矩阵。

> **语法:** `sympy.combinatorics.partitions.RGS_generalized(m)`
> **返回:**返回一个 m+1 大小的矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.combinatorics.partitions.RGS_generalized()`方法，我们能够获得无限制的增长字符串，并返回大小为 m+1 的矩阵。

```py
# import sympy and RGS_generalized
from sympy.combinatorics.partitions import RGS_generalized
from sympy import *

# Using sympy.combinatorics.partitions.RGS_generalized() method
gfg = RGS_generalized(3)

print(gfg)
```

**输出:**

> 矩阵(
> [ [1，1，1，1]，
> [1，2，3，0]，
> [2，5，0，0]，
> [5，0，0，0] ])

**例 2 :**

```py
# import sympy and RGS_generalized
from sympy.combinatorics.partitions import RGS_generalized
from sympy import *

# Using sympy.combinatorics.partitions.RGS_generalized() method
gfg = RGS_generalized(6)

print(gfg)
```

**输出:**

> 矩阵(
> [ [1，1，1，1，1，1，1]，
> [1，2，3，4，5，6，0]，
> [2，5，10，17，26，0，0]，
> [5，15，37，77，0，0，0，0，0]，
> [15，52，151，0，0，0，0，0]，
> [52，203，0，0，0，0