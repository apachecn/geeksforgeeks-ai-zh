# Python | Numpy np.hermeval3d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm eval 3d-method/](https://www.geeksforgeeks.org/python-numpy-np-hermeval3d-method/)

借助`**np.hermeval3d()**`方法，我们可以在点(x，y，z)上计算一个三维埃尔米特级数，其中(x，y，z)在`np.hermeval3d()`方法中定义。

> **语法:** `np.hermeval3d(x, y, series)`
> **返回:**返回评估后的三维厄米系列。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermeval3d()`方法，我们能够使用该方法来评估 x、y 和 z 上的 3-D hermite 级数。

```py
# import numpy and hermeval3d
import numpy as np
from numpy.polynomial.hermite_e import hermeval3d

series = np.array([[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]])
# using np.hermeval3d() method
gfg = hermeval3d(3, 4, 6, series)

print(gfg)
```

**输出:**

> Eight thousand six hundred and sixteen

**例 2 :**

```py
# import numpy and hermeval3d
import numpy as np
from numpy.polynomial.hermite_e import hermeval3d

series = np.array([[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]])
# using np.hermeval3d() method
gfg = hermeval3d([0, 1], [2, 3], [4, 5], series)

print(gfg)
```

**输出:**

> [1240\. 1566.]