# Python | Numpy np.chebmulx()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-chebmulx-method/](https://www.geeksforgeeks.org/python-numpy-np-chebmulx-method/)

借助`**np.chebmulx()**`方法，利用`np.chebmulx()`方法可以得到**切比雪夫级数**与自变量 x 的乘积。

> **语法:** `np.chebmulx(s1)`
> **返回:**与 x 相乘后返回一个数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.chebmulx()`方法，我们能够使用该方法获得切比雪夫级数与自变量 x 的乘积。

```
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (4, 6, 8)

# using np.chebmulx() method
gfg = C.chebmulx(s1)

print(gfg)
```

**输出:**

> [3\. 8\. 3\. 4.]

**例 2 :**

```
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (4, 6, 8, 1, 3, 5)

# using np.chebmulx() method
gfg = C.chebmulx(s1)

print(gfg)
```

**输出:**

> [3\. 8\. 3.5 5.5 3\. 1.5 2.5]