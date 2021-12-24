# Python | sympy。矩阵行()方法

> 原文:[https://www . geesforgeks . org/python-sympy-matrix-row-method/](https://www.geeksforgeeks.org/python-sympy-matrix-row-method/)

借助`**sympy.Matrix.row()**`方法，我们可以提取矩阵的行。

> **语法:** `sympy.Matrix.row()`
> **返回:**返回一个矩阵的行。

**示例#1 :**

In the given example we can see that the `sympy.Matrix().row()` method is used to extract the rows of a matrix.

```
# Import all the methods from sympy
from sympy import *

# use the row() method for matrix
gfg_val = Matrix([[1, 2], [2, 1]]).row(1)

print(gfg_val)
```

**输出:**

> [2, 1]

**例 2 :**

```
from sympy import *

# use the row() method for matrix
gfg_val = Matrix([[1, 2], [2, 3], [23, 45]]).row(2)

print(gfg_val)
```

**输出:**

> [23, 45]