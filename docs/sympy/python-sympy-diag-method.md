# Python | sympy.diag()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-diag-method/](https://www.geeksforgeeks.org/python-sympy-diag-method/)

借助`**sympy.diag()**`方法，我们可以用`sympy.diag()`方法创建一个维数为 nxn，对角线上填充数字的矩阵。

> **语法:** `sympy.diag()`
> **返回:**返回新矩阵。

**示例#1 :**
在本例中，我们可以看到，通过使用`sympy.diag()`方法，我们能够创建一个矩阵，该矩阵的维数 nxn 全部用传入参数的对角线上的数字填充。

```py
# import sympy
from sympy import *

# Use sympy.diag() method
mat = diag(3, 4)

print(mat)
```

**输出:**

> 矩阵([
> [3，0]，
> [0，4]])

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.diag() method
mat = diag(3, 4, 5, 8)

print(mat)
```

**输出:**

> 矩阵([
> [3，0，0，0]，
> [0，4，0，0]，
> [0，0，5，0]，
> [0，0，0，8]])