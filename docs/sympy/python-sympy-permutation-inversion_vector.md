# Python | SymPy placement . inversion _ vector()

> 原文:[https://www . geesforgeks . org/python-sympy-排列-反转 _vector/](https://www.geeksforgeeks.org/python-sympy-permutation-inversion_vector/)

 **arrangement . inversion_vector():inversion _ vector()**是一个 sympy Python 库函数，返回参数中排列的 inversion _ vector 值。
反转向量包括那些其值指示排列中的元素数量的元素，它们是<它并且位于它的右侧。

> **语法:**
> sympy . combinations .排列.置换. inversion_vector()
> 
> **返回:**
> 置换的逆向量值

**代码#1 : inversion_vector()示例**

```
# Python code explaining
# SymPy.Permutation.inversion_vector()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.inversion_vector() method 

# creating Permutation
a = Permutation([[2, 0], [3, 1]])

b = Permutation([1, 3, 5, 4, 2, 0])

print ("Permutation a - inversion_vector form : ", a.inversion_vector())
print ("Permutation b - inversion_vector form : ", b.inversion_vector())
```

**输出:**

> 排列 a–反转 _ 向量形式:[2，2，0]
> 排列 b–反转 _ 向量形式:[1，2，3，2，1]

**代码#2:反转 _ 向量()示例**–2D 置换

```
# Python code explaining
# SymPy.Permutation.inversion_vector()

# importing SymPy libraries
from sympy.combinatorics.partitions import Partition
from sympy.combinatorics.permutations import Permutation

# Using from sympy.combinatorics.permutations.Permutation.inversion_vector() method 

# creating Permutation
a = Permutation([[2, 4, 0], 
                 [3, 1, 2],
                 [1, 5, 6]])

print ("Permutation a - inversion_vector form : ", a.inversion_vector())
```

**输出:**

> 排列 a–反转向量形式:[3，2，2，2，0，1]