# Python 中的 SymPy | Partition.next_lex()

> 原文:[https://www . geesforgeks . org/sympy-partition-next _ lex-in-python/](https://www.geeksforgeeks.org/sympy-partition-next_lex-in-python/)

**partition . next _ lex():next _ lex()**是一个 sympy Python 库函数，返回下一个整数分区，n 按 lexographical 顺序。如果分区是[1，…，1]，这种排序将环绕[n]。

> **语法:**sympy . combinations . partitions . partition . next _ lex()
> 
> **返回:**下一个整数分区，n 按字母顺序排列

**代码#1 : next_lex()示例**

```py
# Python code explaining
# SymPy.next_lex()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import IntegerPartition

# Using from sympy.combinatorics.partitions.Partition.next_lex() method 
p = IntegerPartition([312, 121, 14, 5])

print('p : ', p)
print('\nNext Integrer : ', p.next_lex())
```

**输出:**

> p : [312，121，14，5]
> 
> 下一个积分 ： [312， 121， 15， 1， 1， 1， 1]

**代码#2 : next_lex()示例**

```py
# Python code explaining
# SymPy.next_lex()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.partitions import IntegerPartition

# Using from sympy.combinatorics.partitions.Partition.next_lex() method 
p = IntegerPartition([1, 312, 121, 14, 
                      34, 56, 32])

print('p : ', p)
print('\nNext Integrer : ', p.next_lex())
```

**输出:**

> p : [312，121，56，34，32，14，1]
> 
> 下一个积分 ： [312， 121， 56， 34， 32， 15]