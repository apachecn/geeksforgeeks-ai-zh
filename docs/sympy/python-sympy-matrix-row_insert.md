# Python | sympy。矩阵()。row_insert()

> 原文:[https://www . geesforgeks . org/python-sympy-matrix-row _ insert/](https://www.geeksforgeeks.org/python-sympy-matrix-row_insert/)

借助`**Matrix().row_insert()**`方法，我们可以在维数为 nxm 的矩阵中插入一行，其中插入行的维数为 1xm。

> **语法:** `Matrix().row_insert()`
> **返回:**返回新矩阵。

**示例#1 :**
在本例中，我们能够使用`Matrix().row_insert()`方法在矩阵中插入一行。

```py
# Import all the methods from sympy
from sympy import *

# Make a matrix
gfg_mat = Matrix([[1, 2], [2, 1]])

# use the row_insert() method for matrix
new_mat = gfg_mat.row_insert(1, Matrix([[3, 4]]))

print(new_mat)
```

**输出:**

> 矩阵([[1，2]，[3，4]，[2，1]]

**例 2 :**

```py
# Import all the methods from sympy
from sympy import *

# Make a matrix
gfg_mat = Matrix([[1, 2], [2, 1]])

# use the row_insert() method for matrix
new_mat = gfg_mat.row_insert(2, Matrix([[13, 24]]))

print(new_mat)
```

**输出:**

> 矩阵([[1，2]，[2，1]，[13，24]]