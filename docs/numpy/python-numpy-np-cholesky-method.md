# Python | Numpy np.cholesky()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-chole sky-method/](https://www.geeksforgeeks.org/python-numpy-np-cholesky-method/)

借助`**np.cholesky()**`方法，我们可以利用`np.cholesky()`方法得到 cholesky 分解。

> **语法:** `np.cholesky(matrix)`
> **返回:**返回乔莱斯基分解。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.cholesky()`方法，我们能够使用该方法获得矩阵形式的 cholesky 分解。

```py
# import numpy
import numpy as np

a = np.array([[2, -3j], [5j, 15]])
# using np.cholesky() method
gfg = np.linalg.cholesky(a)

print(gfg)
```

**输出:**

> [[1.41421356 + 0.j，0。+0 . j]
> 【0。+ 3.53553391j，1.58113883 + 0.j]]

**例 2 :**

```py
# import numpy
import numpy as np

a = np.array([[12, -13j], [4j, 8]])
# using np.cholesky() method
gfg = np.linalg.cholesky(a)

print(gfg)
```

**输出:**

> [[3.46410162 + 0.j，0。+0 . j]
> 【0。+ 1.15470054j，2.5819889 + 0.j]]