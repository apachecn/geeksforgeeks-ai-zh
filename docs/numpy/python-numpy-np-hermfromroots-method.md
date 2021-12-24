# Python | Numpy NP . herm from roots()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm from roots-method/](https://www.geeksforgeeks.org/python-numpy-np-hermfromroots-method/)

借助`**np.hermfromroots()**`方法，利用`np.hermfromroots()`方法可以从给定的根中得到厄米级数系数。

> **语法:** `np.hermfromroots(roots)`
> **返回:**返回埃尔米特级数的系数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermfromroots()`方法，我们能够通过使用这个方法从给定的根中得到厄米级数的系数。

```
# import numpy and hermfromroot
import numpy as np
from numpy.polynomial.hermite import hermfromroots

roots = np.array([0.1, 2, 0.3, 4])
# using np.hermfromroots() method
gfg = hermfromroots(roots)

print(gfg)
```

**输出:**

> [6.205 -6.49 3.3575 -0.8 0.0625]

**例 2 :**

```
# import numpy and hermfromroot
import numpy as np
from numpy.polynomial.hermite import hermfromroots

roots = np.array([1, 2, 3, 4, 1.0001])
# using np.hermfromroots() method
gfg = hermfromroots(roots)

print(gfg)
```

**输出:**

> [-7.4754225 e+01 7.2628250 e+01-2.9500950 e+01 6.2501250 e+00
> -6.8750625 e-01 3.1250000 e-02]