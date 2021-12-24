# Python | Numpy np.herm2poly 方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm 2 poly-method/](https://www.geeksforgeeks.org/python-numpy-np-herm2poly-method/)

借助`**np.herm2poly()**`方法，我们可以利用`np.herm2poly()`方法从埃尔米特级数中得到多项式。

> **语法:** `np.herm2poly(hermite series)`
> **返回:**返回多项式的系数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.herm2poly()`方法，我们能够使用该方法从埃尔米特级数中获得多项式的系数。

```py
# import numpy and herm2poly
import numpy as np
from numpy.polynomial.hermite import herm2poly

x = np.array([0.1, 0.2, 0.3, 0.4, 0.5])
# using np.herm2poly() method
gfg = herm2poly(x)

print(gfg)
```

**输出:**

> [5.5 -4.4 -22.8 3.2 8.]

**例 2 :**

```py
# import numpy and herm2poly
import numpy as np
from numpy.polynomial.hermite import herm2poly

x = np.array([-0.5, -0.4, -0.3, -0.2, -0.1, 0, 0.1, 0.2, 0.3, 0.4, 0.5])
# using np.herm2poly() method
gfg = herm2poly(x)

print(gfg)
```

**输出:**

> 【-14629.1 11761.6 147243.6-31585.6-197617.6 19084.8 79571.2
> -3660.8-11443.2 204.8 512。]