# Python | Numpy np.hermvander2d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm vander2d-method/](https://www.geeksforgeeks.org/python-numpy-np-hermvander2d-method/)

借助于`**np.hermvander2d()**`方法，我们可以利用`np.hermvander2d()`方法从给定度数的埃尔米特级数中得到二维伪范德蒙矩阵。

> **语法:** `np.hermvander2d(x, y, deg)`
> **返回:**返回给定度数的二维伪范德蒙矩阵。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermvander2d()`方法，我们能够利用这个方法得到埃尔米特级数的二维伪范德蒙矩阵。

```py
# import numpy and hermvander2d
import numpy as np
from numpy.polynomial.hermite import hermvander2d

x = np.array([1, 2])
y = np.array([-1, -2])
x_deg, y_deg = 2, 2

# using np.hermvander2d() method
gfg = hermvander2d(x, y, [x_deg, y_deg])

print(gfg)
```

**输出:**

> [[ 1.-2.2.2.-4.4.2.-4.4.】
> 【1。-4.14.4.-16.56.14.-56.196.]]

**例 2 :**

```py
# import numpy and hermvander2d
import numpy as np
from numpy.polynomial.hermite import hermvander2d

x = np.array([0.5, 0.10, 0.10, 0.5])
y = np.array([1, 2, 3, 5])
x_deg, y_deg = 1, 1

# using np.hermvander2d() method
gfg = hermvander2d(x, y, [x_deg, y_deg])

print(gfg)
```

**输出:**

> [[ 1.2.1.2.】
> 【1。4.0.2 0.8]
> 【1。6.0.2 1.2]
> 【1。10.1.10.]]