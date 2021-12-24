# Python | Numpy np.eigvals()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-EIG vals-method/](https://www.geeksforgeeks.org/python-numpy-np-eigvals-method/)

借助`**np.eigvals()**`方法，我们可以用`np.eigvals()`方法得到一个矩阵的特征值。

> **语法:** `np.eigvals(matrix)`
> **返回:**返回矩阵的特征值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.eigvals()`方法，我们能够使用该方法获得矩阵的特征值。

```
# import numpy
from numpy import linalg as LA

# using np.eigvals() method
gfg = LA.eigvals([[1, 2], [3, 4]])

print(gfg)
```

**输出:**

> [-0.37228132 5.37228132]

**例 2 :**

```
# import numpy
from numpy import linalg as LA

# using np.eigvals() method
gfg = LA.eigvals([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

print(gfg)
```

**输出:**

> [1.61168440 e+01-1.11684397 e+00-1.30367773e-15]