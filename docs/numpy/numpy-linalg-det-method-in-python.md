# Python 中的 numpy.linalg.det()方法

> 原文:[https://www . geesforgeks . org/numpy-linalg-det-method-in-python/](https://www.geeksforgeeks.org/numpy-linalg-det-method-in-python/)

在 NumPy 中，我们可以借助 **numpy.linalg.det()计算给定方阵的行列式。**它会把给定的方阵作为参数，并返回它的行列式。

> **语法:** numpy.linalg.det()
> **参数:**一个方阵。
> **返回:**那个方阵的行列式。

**例 1:**

## 计算机编程语言

```
import numpy as np
from numpy import linalg as LA

array1 = np.array([[1, 2], [3, 4]])

# Original 2-d array
print(array1)

# Determinant of the said 2-D array
print(np.linalg.det(array1))
```

**输出:**

```
[[1 2]
 [3 4]]
-2.0000000000000004
```

**例 2:**

## 计算机编程语言

```
import numpy as np
from numpy import linalg as LA

array1 = np.array([[1, 2, 3], [3, 4, 1], [3, 2, 1]])

# Original 2-d array
print(array1)

# Determinant of the said 2-D array
print(np.linalg.det(array1))
```

**输出:**

```
[[1 2 3]
 [3 4 1]
 [3 2 1]]
-15.999999999999998
```