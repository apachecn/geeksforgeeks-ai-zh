# Python | Numpy np.hermtrim()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm trim-method/](https://www.geeksforgeeks.org/python-numpy-np-hermtrim-method/)

借助`**np.hermtrim()**`方法，我们可以使用`np.hermtrim()`方法修剪一系列埃尔米特系数中的尾值。

> **语法:** `np.hermtrim(series, tol)`
> 
> **返回:**修剪后返回级数的系数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermtrim()`方法，我们能够使用该方法获得修剪后的埃尔米特级数。

```py
# import numpy and hermtrim
import numpy as np
from numpy.polynomial.hermite import hermtrim

series = np.array([2, 0, 4, 0, 6, 1, 1, 1])

# using np.hermtrim() method
gfg = hermtrim(series, tol = 1)

print(gfg)
```

**输出:**

> [2\. 0\. 4\. 0\. 6.]

**例 2 :**

```py
# import numpy and hermtrim
import numpy as np
from numpy.polynomial.hermite import hermtrim

series = np.array([1, 0, 0, 0, 0, 0])

# using np.hermtrim() method
gfg = hermtrim(series, tol = 0)

print(gfg)
```

**输出:**

> [1.]