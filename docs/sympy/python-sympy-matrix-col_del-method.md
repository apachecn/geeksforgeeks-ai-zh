# Python | sympy。Matrix.col_del()方法

> 原文:[https://www . geesforgeks . org/python-sympy-matrix-col _ del-method/](https://www.geeksforgeeks.org/python-sympy-matrix-col_del-method/)

借助`**sympy.Matrix.col_del()**`方法，我们可以删除矩阵的列。

> **语法:** `sympy.Matrix().col_del()`
> **返回:**返回新矩阵。

**示例#1 :**
在给定的示例中，我们可以看到`sympy.Matrix.col_del()`方法用于删除矩阵的列并返回新的矩阵。

```
# Import all the methods from sympy
from sympy import *

# use the col_del() method for matrix
gfg_val = Matrix([[1, 2], [2, 1]]).col_del(1)

print(gfg_val)
```

**输出:**

> 矩阵([[1]，[2]])

**例 2 :**

```
from sympy import *

# use the col() method for matrix
gfg_val = Matrix([[1, 2], [2, 3], [23, 45]]).col_del(1)

print(gfg_val)
```

**输出:**

> 矩阵([[2]，[3]，[45]]