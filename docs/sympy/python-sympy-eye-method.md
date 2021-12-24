# Python | symy . eye()方法

> 原文:[https://www.geeksforgeeks.org/python-sympy-eye-method/](https://www.geeksforgeeks.org/python-sympy-eye-method/)

借助`**sympy.eye()**`方法，我们可以用`sympy.eye()`方法求出恒等式矩阵。

> **语法:** `sympy.eye()`
> **返回:**返回一个身份矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.eye()`方法，我们能够找到维数为 nxn 的恒等式矩阵，其中 n 将作为参数传递。

```
# import sympy
from sympy import *

# Use sympy.eye() method
mat = eye(3)

print(mat)
```

**输出:**

> 矩阵([
> [1，0，0]，
> [0，1，0]，
> [0，0，1]])

**例 2 :**

```
# import sympy
from sympy import *

# Use sympy.eye() method
mat = eye(5)

print(mat)
```

**输出:**

> 矩阵([
> [1，0，0，0，0]，
> [0，1，0，0，0]，
> [0，0，1，0，0]，
> [0，0，0，1，0]，
> [0，0，0，0，1]])