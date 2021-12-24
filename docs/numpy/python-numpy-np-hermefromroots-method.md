# Python | Numpy NP . hermefrom root()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-NP-hermefrom root-method/](https://www.geeksforgeeks.org/python-numpy-np-hermefromroots-method/)

借助`**np.hermefromroots()**`方法，我们可以利用`np.hermefromroots()`方法从给定的根得到 hermiteE 级数。

> **语法:** `np.hermefromroots(roots)`
> **返回:**返回 hermiteE 系列。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermefromroots()`方法，我们能够使用该方法从给定的根获得 hermiteE 级数。

```
# import numpy and hermefromroots
import numpy as np
from numpy.polynomial.hermite_e import hermefromroots

series = np.array([0.1, 0.2, 0.3, 0.4, 0.5])
# using np.hermefromroots() method
gfg = hermefromroots(series)

print(gfg)
```

**输出:**

> [-4.7262 17.5774 -9.225 10.85 -1.5 1.]

**例 2 :**

```
# import numpy and hermefromroots
import numpy as np
from numpy.polynomial.hermite_e import hermefromroots

series = np.array([1, 0, 0, 1, 1, 0])
# using np.hermefromroots() method
gfg = hermefromroots(series)

print(gfg)
```

**输出:**

> [24\. -48\. 63\. -31\. 18\. -3\. 1.]