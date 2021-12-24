# Python | Numpy np.chebder()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-cheb der-method/](https://www.geeksforgeeks.org/python-numpy-np-chebder-method/)

借助`**np.chebder()**`方法，我们可以利用`np.chebder()`方法，以具有坐标值的数组形式得到切比雪夫级数的微分值。

> **语法:** `np.chebder(series, value)`
> **返回:**微分后返回具有数列坐标的数组。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.chebder()`方法，我们能够得到切比雪夫级数的微分，它将返回一个有坐标的数组。

```py
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

x = np.array([1, 2, 3])
# using np.chebder() method
gfg = C.chebder(x, 2)

print(gfg)
```

**输出:**

```py
[ 12.]

```

**例 2 :**

```py
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

x = np.array([2, 5, 7, 11])
# using np.chebder() method
gfg = C.chebder(x, 2)

print(gfg)
```

**输出:**

```py
[  28\.  264.]

```