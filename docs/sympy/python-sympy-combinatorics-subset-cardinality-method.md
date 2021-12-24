# Python | sympy . combinations . subset()。基数法

> 原文:[https://www . geesforgeks . org/python-sympy-combinations-subset-cardinality-method/](https://www.geeksforgeeks.org/python-sympy-combinatorics-subset-cardinality-method/)

借助`**sympy.combinatorics.Subset().cardinality**`方法，我们可以用`sympy.combinatorics.Subset().cardinality`方法求出子集的总基数。

> **语法:** `sympy.combinatorics.Subset().cardinality`
> **返回:**返回子集的总基数。

**示例#1 :**
在这个示例中我们可以看到，通过使用`sympy.combinatorics.Subset().cardinality`方法，我们能够得到子集的总基数。

```py
# import sympy and subset
from sympy.combinatorics.subsets import Subset

# Using sympy.combinatorics.Subset().cardinality method
gfg = Subset(['c', 'e'], ['a', 'b', 'c', 'e'])

print(gfg.cardinality)
```

**输出:**

> Sixteen

**例 2 :**

```py
# import sympy and subset
from sympy.combinatorics.subsets import Subset

# Using sympy.combinatorics.Subset().cardinality method
gfg = Subset(['c', 'e', 'f'], ['a', 'f', 'c', 'e'])

print(gfg.cardinality)
```

**输出:**

> Sixteen