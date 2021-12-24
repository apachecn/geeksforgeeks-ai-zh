# Python | sympy.zeros()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-zeros-method/](https://www.geeksforgeeks.org/python-sympy-zeros-method/)

借助`**sympy.zeros()**`方法，我们可以使用`sympy.zeros()`方法创建一个维数为 nxm 且填充零的矩阵。

> **语法:** `sympy.zeros()`
> **返回:**返回一个零矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.zero()`方法，我们能够创建维度 nxn 全部用零填充的零矩阵，其中 nxm 将作为参数传递。

```py
# import sympy
from sympy import *

# Use sympy.zero() method
mat = zeros(3, 4)

print(mat)
```

**输出:**

> 矩阵([
> [0，0，0，0]，
> [0，0，0，0]，
> [0，0，0，0]])

**例 2 :**

```py
# import sympy
from sympy import *

# Use sympy.zero() method
mat = zeros(2, 4)

print(mat)
```

**输出:**

> 矩阵([[0，0，0，0]，
> [0，0，0，0]])