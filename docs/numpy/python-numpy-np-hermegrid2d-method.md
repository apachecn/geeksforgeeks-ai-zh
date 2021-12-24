# python | num py NP . hermgrid 2d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermegrid 2d-method/](https://www.geeksforgeeks.org/python-numpy-np-hermegrid2d-method/)

借助`**np.hermegrid2d()**`方法，我们可以在(x，y)的笛卡儿积上求一个二维埃尔米特级数，其中(x，y)是在`np.hermegrid2d()`方法中定义的。

> **语法:** `np.hermegrid2d(x, y, series)`
> **返回:**返回评估后的二维厄米特级数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermegrid2d()`方法，我们能够用这个方法来评估 x 和 y 的笛卡尔乘积上的 2-D hermite 级数。

```py
# import numpy and hermegrid2d
import numpy as np
from numpy.polynomial.hermite_e import hermegrid2d

series = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])
# using np.hermegrid2d() method
gfg = hermegrid2d(3, 4, series)

print(gfg)
```

**输出:**

> One thousand nine hundred and twelve

**例 2 :**

```py
# import numpy and hermegrid2d
import numpy as np
from numpy.polynomial.hermite_e import hermegrid2d

series = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])
# using np.hermegrid2d() method
gfg = hermegrid2d([2, 3], [5, 6], series)

print(gfg)
```

**输出:**

> [[2689.4650.】
> 【3772。6520.]]