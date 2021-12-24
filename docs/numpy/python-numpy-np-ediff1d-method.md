# Python | Numpy np.ediff1d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-ediff 1d-method/](https://www.geeksforgeeks.org/python-numpy-np-ediff1d-method/)

借助`**np.ediff1d()**`方法，我们可以利用`np.ediff1d()`方法得到两个连续元素之间差异的 1D 数组。

> **语法:** `np.ediff1d(array)`
> **返回:**返回连续元素有差异的 1D 阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.ediff1d()`方法，我们能够使用该方法获得数组元素的连续差异的 1D 数组。

```py
# import numpy
import numpy as np

# using np.ediff1d() method
arr = np.array([1, 2, 3, 5, 7, 11])
gfg = np.ediff1d(arr)

print(gfg)
```

**输出:**

> [1 1 2 2 4]

**例 2 :**

```py
# import numpy
import numpy as np

# using np.ediff1d() method
arr = np.array([1, 2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47])
gfg = np.ediff1d(arr)

print(gfg)
```

**输出:**

> [1 1 2 2 4 2 4 2 4 6 2 6 4 2 4]