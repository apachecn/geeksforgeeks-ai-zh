# Python | Numpy np.as_series()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-as _ series-method/](https://www.geeksforgeeks.org/python-numpy-np-as_series-method/)

借助`**np.as_series()**`方法，我们可以利用`np.as_series()`方法从多维数组中得到一个一维序列。

> **语法:** `np.as_series(array)`
> **返回:**返回一个一维序列。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.as_series()`方法，我们能够使用该方法从多维数组中获得一维序列。

```py
# import numpy and as_series
import numpy as np
from numpy.polynomial import polyutils as pu

arr = np.array([0.1, 0.2, 0.3])

# using np.as_series() method
gfg = pu.as_series(arr)

print(gfg)
```

**输出:**

> [数组([0.1])，数组([0.2])，数组([0.3])]

**例 2 :**

```py
# import numpy and as_series
import numpy as np
from numpy.polynomial import polyutils as pu

arr = np.array([[0.1, 0.2, 0.3], [1, 2, 3]])

# using np.as_series() method
gfg = pu.as_series(arr)

print(gfg)
```

**输出:**

> [数组([0.1，0.2，0.3])，数组([1。, 2., 3.])]