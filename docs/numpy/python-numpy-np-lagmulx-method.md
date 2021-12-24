# Python | Numpy np.lagmulx()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag mulx-method/](https://www.geeksforgeeks.org/python-numpy-np-lagmulx-method/)

借助`**np.lagmulx()**`方法，我们可以利用`np.lagmulx()`方法得到拉盖尔级数与 x 的乘积，其中 x 为自变量。

> **语法:** `np.lagmulx(series)`
> **返回:**返回级数相乘后的系数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.lagmulx()`方法，我们能够用这个方法得到拉盖尔级数与自变量 x 相乘后的级数系数。

```py
# import numpy and lagmulx
import numpy as np
from numpy.polynomial.laguerre import lagmulx

series = np.array([1, 2, 3, 4, 5])

# using np.lagmulx() method
gfg = lagmulx(series)

print(gfg)
```

**输出:**

> [ -1\. -1\. -1\. -1\. 29\. -25.]

**例 2 :**

```py
# import numpy and lagmulx
import numpy as np
from numpy.polynomial.laguerre import lagmulx

series = np.array([10, 20, 30])

# using np.lagmulx() method
gfg = lagmulx(series)

print(gfg)
```

**输出:**

> [ -10\. -10\. 110\. -90.]