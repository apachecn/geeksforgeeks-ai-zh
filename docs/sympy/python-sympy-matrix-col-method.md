# Python | sympy。Matrix.col()方法

> 原文:[https://www . geesforgeks . org/python-sympy-matrix-col-method/](https://www.geeksforgeeks.org/python-sympy-matrix-col-method/)

借助`**sympy.Matrix().col()**`方法，我们可以提取矩阵的列。

> **语法:** `sympy.Matrix().col()`
> **返回:**返回矩阵的 col。

**示例#1 :**
在给定的示例中，我们可以看到`sympy.Matrix.col()`方法用于提取矩阵的列。

```
# Import all the methods from sympy
from sympy import *

# use the col() method for matrix
gfg_val = Matrix([[1, 2], [2, 1]]).col(1)

print(gfg_val)
```

**输出:**

> 矩阵([[2]，[1]])

**例 2 :**

```
from sympy import *

# use the col() method for matrix
gfg_val = Matrix([[1, 2], [2, 3], [23, 45]]).col(0)

print(gfg_val)
```

**输出:**

> 矩阵([[1]，[2]，[23]])