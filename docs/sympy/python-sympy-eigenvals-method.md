# Python | sympy .特征值()方法

> 原文:[https://www . geesforgeks . org/python-sympy-eignvals-method/](https://www.geeksforgeeks.org/python-sympy-eigenvals-method/)

借助`**sympy.eigenvals()**`方法，我们可以用`sympy.eigenvals()`方法求出一个矩阵的特征值。

> **语法:** `sympy.eigenvals()`
> **返回:**返回矩阵的特征值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`sympy.eigenvals()`方法，我们能够找到矩阵的特征值。

```
# import sympy
from sympy import *

# Use sympy.eigenvals() method
mat = Matrix([[1, 0, 1], [2, -1, 3], [4, 3, 2]])
d = mat.eigenvals()

print(d)
```

**输出:**

> { 2/3+46/(9 *(241/54+sqrt(36807)* I/18)* *(1/3))+(241/54+sqrt(36807)* I/18)* *(1/3):1.2/3+46/(9)*(-1/2+sqrt(3)* I/2)*(241/54+sqrt(36807)* I/18)* *(1/3))+(-1/2+sqrt(3)* I/2)*(241/54+sqrt(36807

**例 2 :**

```
# import sympy
from sympy import *

# Use sympy.eigenvals() method
mat = Matrix([[1, 5, 1], [12, -1, 31], [4, 33, 2]])
d = mat.eigenvals()

print(d)
```

**输出:**

> { 2/3+3268/(9 *(16225/54+sqrt(154826967)* I/18)* *(1/3))+(16225/54+sqrt(154826967)* I/18)* *(1/3):1.2/3+3268/(9)*(-1/2+sqrt(3)* I/2)*(16225/54+sqrt(154826967)* I/18)* *(1/3))+(-1/2+sqrt(3)* I/2)* *