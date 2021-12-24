# Python | Numpy np.hermeval2d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm eval 2d-method/](https://www.geeksforgeeks.org/python-numpy-np-hermeval2d-method/)

借助`**np.hermeval2d()**`方法，我们可以在点(x，y)上求一个二维埃尔米特级数，其中(x，y)在`np.hermeval2d()`方法中定义。

> **语法:** `np.hermeval2d(x, y, series)`
> **返回:**返回评估后的二维厄米特级数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermeval2d()`方法，我们能够使用这个方法来评估 x 和 y 上的 2-D hermite 级数。

```py
# import numpy and hermeval2d
import numpy as np
from numpy.polynomial.hermite_e import hermeval2d

series = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])
# using np.hermeval2d() method
gfg = hermeval2d(3, 4, series)

print(gfg)
```

**输出:**

> One thousand nine hundred and twelve

**例 2 :**

```py
# import numpy and hermeval2d
import numpy as np
from numpy.polynomial.hermite_e import hermeval2d

series = np.array([[1, 2, 3, 4], [5, 6, 7, 8]])
# using np.hermeval2d() method
gfg = hermeval2d([2, 3], [5, 6], series)

print(gfg)
```

**输出:**

> [2689\. 6520.]