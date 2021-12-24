# Python | Numpy np.lagval()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag val-method/](https://www.geeksforgeeks.org/python-numpy-np-lagval-method/)

借助`**np.lagval()**`方法，利用`np.lagval()`方法可以得到 x 点的拉盖尔级数。

> **语法:** `np.lagval(x, c)`
> **返回:**在 x 点返回拉盖尔级数。

**例#1 :**
在这个例子中我们可以看到，通过使用 **np.lagval()** 方法，我们能够通过使用这个方法得到点 x 处的拉盖尔级数。

```py
# import numpy and lagval
import numpy as np
from numpy.polynomial.laguerre import lagval

x = 2
c = np.array([3, 10])

# import np.lagval() method
gfg = lagval(x, c)

print(gfg)
```

**输出:**

> -7.0

**例 2 :**

```py
# import numpy and lagval
import numpy as np
from numpy.polynomial.laguerre import lagval

x = np.array([[1, 5], [2, 10]])
c = np.array([3, 1])

# import np.lagval() method
gfg = lagval(x, c)

print(gfg)
```

**输出:**

> [[ 3.-1.】
> 【2。-6.]]