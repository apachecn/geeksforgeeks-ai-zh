# Python | sympy。矩阵特征值()方法

> 原文:[https://www . geesforgeks . org/python-sympy-matrix-eignvals-method/](https://www.geeksforgeeks.org/python-sympy-matrix-eigenvals-method/)

借助**症状。矩阵特征值()**方法，我们可以找到矩阵的特征值。

> **句法:**症状。矩阵()。
> **返回:**返回矩阵的特征值。

**示例#1 :**

在给定的例子中，我们可以看到。矩阵特征值()方法用于求矩阵的特征值。

## 蟒蛇 3

```
# Import all the methods from sympy
from sympy import *

# use the eigenvals() method for matrix
gfg_val = Matrix([[1, 2], [2, 1]]).eigenvals()

print(gfg_val)
```

**输出:**

> {3: 1，-1: 1}

**例 2 :**

## 蟒蛇 3

```
from sympy import *

# use the eigenvals() method for matrix
gfg_val = Matrix([[1, 2], [2, 2]]).eigenvals()

print(gfg_val)
```

**输出:**

> { 3/2–sqrt(17)/2:1，3/2+sqrt(17)/2:1 } t0]