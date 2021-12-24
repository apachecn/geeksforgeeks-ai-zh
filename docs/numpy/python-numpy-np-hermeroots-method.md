# Python | Numpy np.hermeroots()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermeroots-method/](https://www.geeksforgeeks.org/python-numpy-np-hermeroots-method/)

借助`**np.hermeroots()**`方法，利用`np.hermeroots()`方法可以得到 hermiteE 级数的根。

> **语法:** `np.hermeroots(series)`
> **返回:**返回 hermiteE 系列的根。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermeroots()`方法，我们能够使用该方法从 hermiteE 系列中获得根。

```py
# import numpy and hermeroots
import numpy as np
from numpy.polynomial.hermite_e import hermeroots

series = np.array([1, 2, 3, 4, 5])
# using np.hermeroots() method
gfg = hermeroots(series)

print(gfg)
```

**输出:**

> [-2.48126206 -0.91457252 0.56384744 2.03198714]

**例 2 :**

```py
# import numpy and hermeroots
import numpy as np
from numpy.polynomial.hermite_e import hermeroots

series = np.array([1, 0, 0, 1, 1, 0])
# using np.hermeroots() method
gfg = hermeroots(series)

print(gfg)
```

**输出:**

> [-2.62826298 -1.12025529 0.6462188 2.10229947]