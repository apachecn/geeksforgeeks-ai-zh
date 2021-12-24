# Python | Numpy np.hermder()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-her mder-method/](https://www.geeksforgeeks.org/python-numpy-np-hermder-method/)

借助`**np.hermder()**`方法，我们可以用`np.hermder()`方法来判别埃尔米特级数。

> **语法:** `np.hermder(series, m)`
> **返回:**返回微分级数的系数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermder()`方法，我们能够利用这个方法得到埃尔米特级数的微分级数系数。

```py
# import numpy and harmder
import numpy as np
from numpy.polynomial.hermite import hermder

series = np.array([2, 0.3, 4, 0.5, 6])
# using np.harmder() method
gfg = hermder(series, m = 1)

print(gfg)
```

**输出:**

> [0.6 16\. 3\. 48.]

**例 2 :**

```py
# import numpy and harmder
import numpy as np
from numpy.polynomial.hermite import hermder

series = np.array([1, 2, 3, 4, 5])
# using np.harmder() method
gfg = hermder(series, m = 2)

print(gfg)
```

**输出:**

> [24\. 96\. 240.]