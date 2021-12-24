# Python | Numpy NP . herm company()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm companion-method/](https://www.geeksforgeeks.org/python-numpy-np-hermcompanion-method/)

借助`**np.hermcompanion()**`方法，我们可以利用`np.hermcompanion()`方法从 hermite 级数中得到伴随矩阵。

> **语法:** `np.hermcompanion(series)`
> **返回:**返回同伴矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermcompanion()`方法，我们能够使用该方法从 hermite 级数中获得伴随矩阵。

```
# import numpy and hermcompanion
import numpy as np
from numpy.polynomial.hermite import hermcompanion

series = np.array([6, 7, 8, 9, 10])
# using np.hermcompanion() method
gfg = hermcompanion(series)

print(gfg)
```

**输出:**

> [[ 0.0.70710678 0.-0.04330127]
> 【0.70710678 0。1.-0.07144345]
> 【0。1.0.1.06144556]
> 【0。0.1.22474487 -0.45 ]]

**例 2 :**

```
# import numpy and hermcompanion
import numpy as np
from numpy.polynomial.hermite import hermcompanion

series = np.array([1, 2, 3, 4, 5])
# using np.hermcompanion() method
gfg = hermcompanion(series)

print(gfg)
```

**输出:**

> [[ 0.0.70710678 0.-0.01443376]
> 【0.70710678 0。1.-0.04082483]
> 【0。1.0.1.10227038]
> 【0。0.1.22474487 -0.4 ]]