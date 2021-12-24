# Python | Numpy np.hermetrim()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm item-method/](https://www.geeksforgeeks.org/python-numpy-np-hermetrim-method/)

借助`**np.hermetrim()**`方法，我们可以使用`np.hermtrim()`方法修剪一系列 hermiteE 系数中的尾值。

> **语法:** `np.hermetrim(series, tol)`
> **返回:**修剪后返回级数的系数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermetrim()`方法，我们能够使用该方法获得修剪后的 hermiteE 系列。

```
# import numpy and herm1trim
import numpy as np
from numpy.polynomial.hermite_e import hermetrim

series = np.array([2, 0, 4, 0, 6, 1, 1, 1])

# using np.hermetrim() method
gfg = hermetrim(series, tol = 1)

print(gfg)
```

**输出:**

> [2\. 0\. 4\. 0\. 6.]

**例 2 :**

```
# import numpy and hermetrim
import numpy as np
from numpy.polynomial.hermite_e import hermetrim

series = np.array([1, 0, 0, 0, 0, 0])

# using np.hermetrim() method
gfg = hermetrim(series, tol = 0)

print(gfg)
```

**输出:**

> [1.]