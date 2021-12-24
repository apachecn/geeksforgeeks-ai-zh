# Python | sympy.det()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-det-method/](https://www.geeksforgeeks.org/python-sympy-det-method/)

借助`**sympy.det()**`方法，我们可以用`sympy.det()`方法求出一个矩阵的行列式。

> **语法:** `sympy.det()`
> **返回:**返回一个矩阵的行列式。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.det()`方法，我们能够找到矩阵的行列式。

```
# import sympy
from sympy import *

# Use sympy.det() method
mat = Matrix([[1, 0, 1], [2, -1, 3], [4, 3, 2]])
d = mat.det()

print(d)
```

**输出:**

> -1

**例 2 :**

```
# import sympy
from sympy import *

# Use sympy.det() method
mat = Matrix([[1, 5, 1], [12, -1, 31], [4, 33, 2]])
d = mat.det()

print(d)
```

**输出:**

> -125