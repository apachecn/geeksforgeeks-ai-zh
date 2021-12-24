# Python | Numpy np.lagfit()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag fit-method/](https://www.geeksforgeeks.org/python-numpy-np-lagfit-method/)

借助`**np.lagfit()**`方法，利用`np.lagfit()`方法可以得到给定数据的拉盖尔级数的最小二乘拟合。

> **语法:** `np.lagfit(x, y, deg)`
> **返回:**返回拉盖尔级数对数据的最小二乘拟合。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.lagfit()`方法，我们能够获得给定数据的拉盖尔级数的最小二乘拟合。

```py
# import numpy and lagfit
import numpy as np
from numpy.polynomial.laguerre import lagfit

x, y = [1, 2], [3, 4]
deg = 2

# import np.lagfit() method
gfg = lagfit(x, y, deg)

print(gfg)
```

**输出:**

> [2.125 -0.125 -1.75]

**例 2 :**

```py
# import numpy and lagfit
import numpy as np
from numpy.polynomial.laguerre import lagfit

x, y = [1, 2, 3], [3, 4, 5]
deg = 3

# import np.lagfit() method
gfg = lagfit(x, y, deg)

print(gfg)
```

**输出:**

> [3.06722689 -0.66386555 -0.40336134 0.40336134]