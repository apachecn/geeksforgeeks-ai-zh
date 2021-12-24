# Python | Sympy 分区。RGS _ unrank()方法

> 原文:[https://www . geesforgeks . org/python-sympy-partitions-rgs _ unlank-method/](https://www.geeksforgeeks.org/python-sympy-partitions-rgs_unrank-method/)

借助`**sympy.combinatorics.partitions.RGS_unrank()**`方法，我们可以得到在`sympy.combinatorics.partitions.RGS_unrank()`方法中作为参数传递的大小的未链接增长字符串。

> **语法:** `sympy.combinatorics.partitions.RGS_unrank()`
> **返回:**返回 m 大小的未链接生长字符串数组

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.combinatorics.partitions.RGS_unrank()`方法，我们能够获得大小为 m 的未链接增长字符串的数组

```
# import sympy and RGS_unrank
from sympy.combinatorics.partitions import RGS_unrank
from sympy import * 

x, y = symbols('x y')

# Using sympy.combinatorics.partitions.RGS_unrank method
gfg = RGS_unrank(51, 8)

print(gfg)
```

**输出:**

> [0, 0, 0, 0, 1, 2, 3, 4]

**例 2 :**

```
# import sympy and RGS_unrank
from sympy.combinatorics.partitions import RGS_unrank
from sympy import * 

x, y = symbols('x y')

# Using sympy.combinatorics.partitions.RGS_unrank method
gfg = RGS_unrank(101, 10)

print(gfg)
```

**输出:**

> [0, 0, 0, 0, 0, 1, 1, 1, 0, 2]