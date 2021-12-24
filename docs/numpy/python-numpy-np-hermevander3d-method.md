# Python | Numpy NP . hermevander3d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermevander3d-method/](https://www.geeksforgeeks.org/python-numpy-np-hermevander3d-method/)

借助`**np.hermevander3d()**`方法，我们可以利用`np.hermevander3d()`方法得到给定的具有 x，y，z 度数的三维数据的伪范德蒙矩阵。

> **语法:** `np.hermevander3d(x, y, z, [x_deg, y_deg, z_deg])`
> 
> **返回:**返回给定三维数据的伪范德蒙矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermevander3d()`方法，我们能够使用该方法获得给定的具有度数(x，y，z)的三维数据的伪范德蒙矩阵。

```py
# import numpy and hermevander3d
import numpy as np
from numpy.polynomial.hermite_e import hermevander3d

x = np.array([1, 0.1])
y = np.array([2, 0.2])
z = np.array([3, 0.3])
x_deg, y_deg, z_deg = 2, 3, 1

# using np.hermevander3d() method
gfg = hermevander3d(x, y, z, [x_deg, y_deg, z_deg])

print(gfg)
```

**输出:**

> [ 1，00000e+00 3，00000e+00 2，00000e+00 3，00000e+00
> 9，00000e+00 2，00000e+00 6，00000e+00 1，00000e+00 3，00000 e+00
> 2，00000e+00 6，00000e+00 3，00000e+00 9，00000e+00 2，00000 e+00

**例 2 :**

```py
# import numpy and hermevander3d
import numpy as np
from numpy.polynomial.hermite_e import hermevander3d

x = np.array([1.01, 2.02, 3.03])
y = np.array([10.1, 20.2, 30.3])
z = np.array([0.1, 0.2, 0.3])
x_deg, y_deg, z_deg = 1, 1, 3

# using np.hermevander3d() method
gfg = hermevander3d(x, y, z, [x_deg, y_deg, z_deg])

print(gfg)
```

**输出:**

> [[ 1.0.1-0.99-0.299 10.1 1.01
> -9.999-3.0199 1.01 0.101-0.9999-0.30199
> 10.201 1.0201-10.09899-3.050099】
> 【1。0.2-0.96-0.592 20.2 4.04
> -19.392-11.9584 2.02 0.404-1.9392-1.19584
> 40.804 8.1608-39.17184-24.155968】
> 【1。0.3-0.91-0.873 30.3 9.09
> -27.573-26.4519 3.03 0.909-2.7573-2.64519
> 91.809 27.5427-83.54619-80.149257]]