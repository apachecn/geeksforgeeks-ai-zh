# Python | Numpy np.hermint()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermin-method/](https://www.geeksforgeeks.org/python-numpy-np-hermint-method/)

借助`**np.hermint()**`方法，我们可以用`np.hermint()`方法积分埃尔米特级数。

> **语法:** `np.hermint(series, m)`
> **返回:**返回积分级数的系数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermint()`方法，我们能够利用这个方法得到埃尔米特级数的积分级数系数。

```py
# import numpy and harmint
import numpy as np
from numpy.polynomial.hermite import hermint

series = np.array([2, 0.3, 4, 0.5, 6])
# using np.harmint() method
gfg = hermint(series, m = 1)

print(gfg)
```

**输出:**

> [-0.6 1\. 0.075 0.66666667 0.0625 0.6]

**例 2 :**

```py
# import numpy and harmint
import numpy as np
from numpy.polynomial.hermite import hermint

series = np.array([1, 2, 3, 4, 5])
# using np.harmint() method
gfg = hermint(series, m = 2)

print(gfg)
```

**输出:**

> [4.5 -2.5 0.125 0.08333333 0.0625 0.05 0.04166667]