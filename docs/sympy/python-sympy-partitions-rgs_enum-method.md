# Python | sympy 分区。RGS_enum()方法

> 原文:[https://www . geesforgeks . org/python-sympy-partitions-rgs _ enum-method/](https://www.geeksforgeeks.org/python-sympy-partitions-rgs_enum-method/)

借助`**sympy.combinatorics.partitions.RGS_enum()**`方法，利用`sympy.combinatorics.partitions.RGS_enum()`方法可以得到大小为 m 的无限制生长串的总数。

> **语法:** `sympy.combinatorics.partitions.RGS_enum(m)`
> **返回:**返回无限制生长字符串总数。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.combinatorics.partitions.RGS_enum()`方法，我们能够得到大小为 m 的无限制生长字符串的总数

```
# import sympy and RGS_generalized
from sympy.combinatorics.partitions import RGS_enum
from sympy import *

# Using sympy.combinatorics.partitions.RGS_enum() method
gfg = RGS_enum(5)

print(gfg)
```

**输出:**

> fifty-two

**例 2 :**

```
# import sympy and RGS_generalized
from sympy.combinatorics.partitions import RGS_enum
from sympy import *

# Using sympy.combinatorics.partitions.RGS_enum() method
gfg = RGS_enum(16)

print(gfg)
```

**输出:**

> Ten billion four hundred and eighty million one hundred and forty-two thousand one hundred and forty-seven