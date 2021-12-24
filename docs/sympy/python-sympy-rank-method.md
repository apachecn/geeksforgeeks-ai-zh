# Python | symy rank()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-rank-method/](https://www.geeksforgeeks.org/python-sympy-rank-method/)

借助`**sympy.combinatorics.Partition().rank**`方法，我们可以得到子阵列的秩，在`sympy.combinatorics.Partition().rank`方法中作为参数传递。

> **语法:** `sympy.combinatorics.Partition().rank`
> **返回:**返回子阵的秩。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.combinatorics.Partition().rank`方法，我们能够获得子阵列的阵列秩。

```
# import sympy and Partition
from sympy.combinatorics.partitions import Partition
from sympy import * x, y = symbols('x y')

# Using sympy.combinatorics.partitions.Partition().rank method
gfg = Partition([1, 2], [4, 5, 6], [-12, -11])

print(gfg.rank)
```

**输出:**

> One hundred and nineteen

**例 2 :**

```
# import sympy and Relational
from sympy.combinatorics.partitions import Partition
from sympy import * x, y = symbols('x y')

# Using sympy.combinatorics.partitions.Partition().rank method
gfg = Partition([3], [1, 91], [2], [6])

print(gfg.rank)
```

**输出:**

> Forty-seven