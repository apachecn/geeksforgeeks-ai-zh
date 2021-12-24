# Python | Numpy np.lagval3d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag val3d-method/](https://www.geeksforgeeks.org/python-numpy-np-lagval3d-method/)

借助`**np.lagval3d()**`方法，利用`np.lagval3d()`方法可以得到 x 点的三维拉盖尔级数。

> **语法:** `np.lagval3d(x, y, z, c)`
> **返回:**在 x、y、z 点返回三维拉盖尔级数

**例#1 :**
在这个例子中我们可以看到，通过使用 **np.lagval3d()** 方法，我们能够通过使用这个方法得到 x，y，z 点的三维拉盖尔级数。

```
# import numpy and lagval3d
import numpy as np
from numpy.polynomial.laguerre import lagval3d

x = np.array([[1, 2], [3, 4]])
y = np.array([[-5, -10], [-15, -20]])
z = np.array([[1, 2], [3, 4]])
c = np.array([1, 2])

# import np.lagval3d() method
gfg = lagval3d(x, y, z, c)

print(gfg)
```

**输出:**

> [[13.44.】
> 【43。94.]]

**例 2 :**

```
# import numpy and lagval3d
import numpy as np
from numpy.polynomial.laguerre import lagval3d

x, y, z = 1, 2, 3
c = np.array([1, 2])

# import np.lagval3d() method
gfg = lagval3d(x, y, z, c)

print(gfg)
```

**输出:**

> One