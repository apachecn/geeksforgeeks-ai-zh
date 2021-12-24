# python | num py NP . hermgrid 3d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermegrid 3d-method/](https://www.geeksforgeeks.org/python-numpy-np-hermegrid3d-method/)

借助`**np.hermegrid3d()**`方法，我们可以在(x，y，z)的笛卡儿积上求一个三维埃尔米特级数，其中(x，y，z)是在`np.hermegrid3d()`方法中定义的。

> **语法:** `np.hermegrid3d(x, y, z, series)`
> **返回:**返回评估后的三维厄米系列。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermegrid3d()`方法，我们能够使用该方法来评估 x、y 和 z 的笛卡尔乘积上的 3-D hermite 级数。

```py
# import numpy and hermegrid3d
import numpy as np
from numpy.polynomial.hermite_e import hermegrid3d

series = np.array([[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]])
# using np.hermegrid3d() method
gfg = hermegrid3d(3, 4, 6, series)

print(gfg)
```

**输出:**

> Eight thousand six hundred and sixteen

**例 2 :**

```py
# import numpy and hermegrid3d
import numpy as np
from numpy.polynomial.hermite_e import hermegrid3d

series = np.array([[1, 2, 3, 4], [5, 6, 7, 8], [9, 10, 11, 12]])
# using np.hermegrid3d() method
gfg = hermegrid3d([0, 1], [2, 3], [4, 5], series)

print(gfg)
```

**输出:**

> [[ 240.316.】
> 【1064。1390.]]