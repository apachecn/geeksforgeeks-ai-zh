# Python | Numpy NP . ma . common _ fill _ value()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-ma-common _ fill _ value-method/](https://www.geeksforgeeks.org/python-numpy-np-ma-common_fill_value-method/)

借助`**np.ma.common_fill_value()**`方法，如果两个掩码数组相同，我们可以使用`np.ma.common_fill_value()`方法从两个掩码数组中获得公共填充值。

> **语法:** `np.ma.common_fill_value(array1, array2)`
> **返回:**返回两个数组的公共填充值。

**示例#1 :**
在本例中，通过使用`np.ma.common_fill_value()`方法，我们能够从两个掩码数组中获得公共填充值。

```py
# import numpy
import numpy as np

x = np.ma.array([1, 2, 3], fill_value = 1)
y = np.ma.array([7, 8, 9], fill_value = 1)

# using np.ma.common_fill_value() method
gfg = np.ma.common_fill_value(x, y)

print(gfg)
```

**输出:**

> one

**例 2 :**

```py
# import numpy
import numpy as np

x = np.ma.array([[1, 2], [2, 1]], fill_value = 2)
y = np.ma.array([[1, 5], [5, 1]], fill_value = 5)

# using np.ma.common_fill_value() method
gfg = np.ma.common_fill_value(x, y)

print(gfg)
```

**输出:**

> 没有人