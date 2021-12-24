# Python | Numpy np.hermevander()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermevander-method/](https://www.geeksforgeeks.org/python-numpy-np-hermevander-method/)

借助`**np.hermevander()**`方法，利用`np.hermevander()`方法可以得到给定度数下的伪范德蒙矩阵。

> **语法:** `np.hermevander(x, deg)`
> **返回:**返回伪范德蒙矩阵。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermevander()`方法，我们能够通过使用这个方法得到给定度数的伪范德蒙矩阵。

```py
# import numpy and hermevander
import numpy as np
from numpy.polynomial.hermite_e import hermevander

x = np.array([0.1, 0.2, 0.3, 0.4, 0.5])
deg = 3
# using np.hermevander() method
gfg = hermevander(x, deg)

print(gfg)
```

**输出:**

> [[ 1.0.1-0.99-0.299]
> 【1。0.2-0.96-0.592]
> 【1。0.3-0.91-0.873]
> 【1。0.4-0.84-1.136]
> 【1。0.5 -0.75 -1.375]]

**例 2 :**

```py
# import numpy and hermevander
import numpy as np
from numpy.polynomial.hermite_e import hermevander

x = np.array([1.1, 2.2, 3.3, 4.4, 5.5])
deg = 3
# using np.hermevander() method
gfg = hermevander(x, deg)

print(gfg)
```

**输出:**

> [[ 1.1.1 0.21-1.969]
> 【1。2.2 3.84 4.048]
> 【1。
> 【1。4.4 18.36 71.984]
> 【1。5.5 29.25 149.875]]