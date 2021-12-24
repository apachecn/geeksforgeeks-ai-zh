# Python | Numpy np.hermvander3d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm vander3d-method/](https://www.geeksforgeeks.org/python-numpy-np-hermvander3d-method/)

借助于`**np.hermvander3d()**`方法，我们可以利用`np.hermvander3d()`方法从给定度数的埃尔米特级数中得到三维伪范德蒙矩阵。

> **语法:** `np.hermvander3d(x, y, z, deg)`
> **返回:**返回给定度数的三维伪范德蒙矩阵。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermvander3d()`方法，我们能够利用这个方法得到埃尔米特级数的三维伪范德蒙矩阵。

```py
# import numpy and hermvander3d
import numpy as np
from numpy.polynomial.hermite import hermvander3d

x = np.array([1, 2])
y = np.array([-1, -2])
z = np.array([1, -2])
x_deg, y_deg, z_deg = 2, 2, 2

# using np.hermvander3d() method
gfg = hermvander3d(x, y, z, [x_deg, y_deg, z_deg])

print(gfg)
```

**输出:**

> [[ 1，000e+00 2，000e+00 -2，000e+00 -4，000e+00 -4，000 e+00
> 2，000e+00 4，000e+00 4，000e+00 2，000e+00 4，000e+00 4，000 e+00
> 4，000e+00 -8，000e+00 -8，000e+00 4，000e+00 8，000 e]

**例 2 :**

```py
# import numpy and hermvander3d
import numpy as np
from numpy.polynomial.hermite import hermvander3d

x = np.array([0.5, 0.10, 0.10, 0.5])
y = np.array([1, 2, 3, 5])
z = np.array([10.1, 20.2, 30.3, -50]) 
x_deg, y_deg, z_deg = 1, 1, 1

# using np.hermvander3d() method
gfg = hermvander3d(x, y, z, [x_deg, y_deg, z_deg])

print(gfg)
```

**输出:**

> 【【1.000 e+00 2.020 e+01 2.000 e+00 4.040 e+01 1.000 e+00 2.020 e+01
> 2.000 e+00 4.040 e+01】
> 【1.000 e+00 4.040 e+01 4.000 e+00 1.616 e+02.000 e-01 8.080 e+00