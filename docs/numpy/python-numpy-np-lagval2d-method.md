# Python | Numpy np.lagval2d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag val2d-method/](https://www.geeksforgeeks.org/python-numpy-np-lagval2d-method/)

借助`**np.lagval2d()**`方法，利用`np.lagval2d()`方法可以得到 x 点的二维拉盖尔级数。

> **语法:** `np.lagval2d(x, y, c)`
> **返回:**在 x 点和 y 点返回二维拉盖尔级数。

**例#1 :**
在这个例子中我们可以看到，通过使用 **np.lagval2d()** 方法，我们能够通过使用这个方法得到点 x 和 y 处的二维拉盖尔级数。

```py
# import numpy and lagval2d
import numpy as np
from numpy.polynomial.laguerre import lagval2d

x = np.array([[1, 2], [3, 4]])
y = np.array([[5, 10], [15, 20]])
c = np.array([1, 2])

# import np.lagval2d() method
gfg = lagval2d(x, y, c)

print(gfg)
```

**输出:**

> [[13.44.】
> 【43。94.]]

**例 2 :**

```py
# import numpy and lagval2d
import numpy as np
from numpy.polynomial.laguerre import lagval2d

x = np.array([[1, 2], [3, 4]])
y = np.array([[-1, -2], [-3, -4]])
c = np.array([1, -2])

# import np.lagval2d() method
gfg = lagval2d(x, y, c)

print(gfg)
```

**输出:**

> [[11.24.】
> 【21。38.]]