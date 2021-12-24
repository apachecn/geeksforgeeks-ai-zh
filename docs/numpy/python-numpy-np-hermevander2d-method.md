# Python | Numpy NP . hermevander2d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermevander2d-method/](https://www.geeksforgeeks.org/python-numpy-np-hermevander2d-method/)

借助`**np.hermevander2d()**`方法，我们可以用`np.hermevander2d()`方法得到给定的具有 x 和 y 度的二维数据的伪范德蒙矩阵。

> **语法:** `np.hermevander2d(x, y, [x_deg, y_deg])`
> **返回:**返回给定二维数据的伪范德蒙矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermevander2d()`方法，我们能够使用该方法获得给定的具有度数(x，y)的二维数据的伪范德蒙矩阵。

```py
# import numpy and hermevander2d
import numpy as np
from numpy.polynomial.hermite_e import hermevander2d

x = np.array([0.1, 0.2])
y = np.array([2, 0.2])
x_deg, y_deg = 2, 3
# using np.hermevander2d() method
gfg = hermevander2d(x, y, [x_deg, y_deg])

print(gfg)
```

**输出:**

> [[ 1.2.3.2.0.1 0.2 0.3 0.2
> -0.99-1.98-2.97-1.98】
> 【1。0.2-0.96-0.592 0.2 0.04-0.192-0.1184
> -0.96-0.192 0.9216 0.56832】]

**例 2 :**

```py
# import numpy and hermevander2d
import numpy as np
from numpy.polynomial.hermite_e import hermevander2d

x = np.array([1.01, 2.02, 3.03])
y = np.array([10.1, 20.2, 30.3])
x_deg, y_deg = 1, 1
# using np.hermevander2d() method
gfg = hermevander2d(x, y, [x_deg, y_deg])

print(gfg)
```

**输出:**

> [[ 1.10.1 1.01 10.201]
> 【1。20.2 2.02 40.804]
> 【1。30.3 3.03 91.809]]