# Python | sympy。Matrix.row_del()方法

> 原文:[https://www . geesforgeks . org/python-sympy-matrix-row _ del-method/](https://www.geeksforgeeks.org/python-sympy-matrix-row_del-method/)

借助`**sympy.Matrix.row_del()**`方法，我们可以删除矩阵的行。

> **语法:** `sympy.Matrix().row_del()`
> **返回:**返回新矩阵。

**示例#1 :**

In the given example we can see that the `sympy.Matrix.row_del()` method is used to delete the row of a matrix and return a new matrix.

```
# Import all the methods from sympy
from sympy import *

# use the row_del() method for matrix
gfg_val = Matrix([[1, 2], [2, 1]]).col_row(1)

print(gfg_val)
```

**输出:**

> 矩阵([1，2])

**例 2 :**

```
from sympy import *

# use the row_del() method for matrix
gfg_val = Matrix([[1, 2], [2, 3], [23, 45]]).row_del(0)

print(gfg_val)
```

**输出:**

> 矩阵([[2，3]，[23，45]])