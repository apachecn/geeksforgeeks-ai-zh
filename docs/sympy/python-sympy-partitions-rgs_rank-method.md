# Python | Sympy 分区。RGS_rank()方法

> 原文:[https://www . geesforgeks . org/python-sympy-partitions-rgs _ rank-method/](https://www.geeksforgeeks.org/python-sympy-partitions-rgs_rank-method/)

借助`**sympy.combinatorics.partitions.RGS_rank()**`方法，我们可以得到`sympy.combinatorics.partitions.RGS_rank()`方法中受限生长串的排名。

> **语法:** `sympy.combinatorics.partitions.RGS_rank()`
> **返回:**返回一个限制成长串的等级。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.combinatorics.partitions.RGS_rank()`方法，我们能够得到受限生长字符串的排名。

```py
# import sympy and RGS_unrank
from sympy.combinatorics.partitions import RGS_rank
from sympy import * x, y = symbols('x y')

# Using sympy.combinatorics.partitions.RGS_rank method
gfg = RGS_rank([1, 2, 5, 4, 2, 10])

print(gfg)
```

**输出:**

> Six hundred and ninety-seven

**例 2 :**

```py
# import sympy and RGS_unrank
from sympy.combinatorics.partitions import RGS_rank
from sympy import * x, y = symbols('x y')

# Using sympy.combinatorics.partitions.RGS_rank method
gfg = RGS_rank([2, 1, 5, 1, 0, 7])

print(gfg)
```

**输出:**

> Three hundred and ninety-two