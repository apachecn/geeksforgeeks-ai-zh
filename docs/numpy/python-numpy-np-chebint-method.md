# Python | Numpy np.chebint()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-chebint-method/](https://www.geeksforgeeks.org/python-numpy-np-chebint-method/)

借助`**np.chebint()**`方法，我们可以用`np.chebint()`方法得到具有坐标值的阵列形式的切比雪夫级数的积分值。

> **语法:** `np.chebint(series, value)`
> **返回:**积分后返回具有级数坐标的数组。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.chebint()`方法，我们能够得到切比雪夫级数的积分，它将返回一个有坐标的数组。

```
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

x = np.array([1, 2, 3])
# using np.chebint() method
gfg = C.chebint(x, 2)

print(gfg)
```

**输出:**

```
[-0.3125      0.25       -0.25        0.08333333  0.0625    ]

```

**例 2 :**

```
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

x = np.array([2, 5, 7, 11])
# using np.chebint() method
gfg = C.chebint(x, 2)

print(gfg)
```

**输出:**

```
[-0.8125     -2.125      -0.66666667 -0.47916667  0.14583333  0.1375    ]

```