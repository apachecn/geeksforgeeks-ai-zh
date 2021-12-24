# Python | numpy . fill _ 对角线()方法

> 原文:[https://www . geesforgeks . org/python-numpy-fill _ 对角线-method/](https://www.geeksforgeeks.org/python-numpy-fill_diagonal-method/)

借助`**numpy.fill_diagonal()**`方法，我们可以用`numpy.fill_diagonal()`方法中作为参数传递的值来填充 numpy 数组的对角线。

> **语法:** `numpy.fill_diagonal(array, value)`
> **返回:**返回数组对角线上的填充值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`numpy.fill_diagonal()`方法，我们能够获得用作为参数传递的值填充的对角线。

```
# import numpy
import numpy as np

# using numpy.fill_diagonal() method
array = np.array([[1, 2], [2, 1]])
np.fill_diagonal(array, 5)

print(array)
```

**输出:**

> [[5 2]
> [2 5]]

**例 2 :**

```
# import numpy
import numpy as np

# using numpy.fill_diagonal() method
array = np.zeros((3, 3), int)
np.fill_diagonal(array, 1)

print(array)
```

**输出:**

> [[1 0 0]
> [0 1 0]
> [0 0 1]]