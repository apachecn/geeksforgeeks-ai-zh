# Python | Numpy np.hermefit()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermefit-method/](https://www.geeksforgeeks.org/python-numpy-np-hermefit-method/)

借助`**np.hermefit()**`方法，利用`np.hermefit()`方法可以得到埃尔米特级数的最小二乘拟合。

> **语法:** `np.hermefit(x, y, deg)`
> **返回:**返回给定数据的最小二乘拟合。

**示例#1 :**
在这个示例中我们可以看到，通过使用`np.hermefit()`方法，我们能够通过使用该方法获得 hermite 级数的最小二乘拟合。

```py
# import numpy and hermefit
import numpy as np
from numpy.polynomial.hermite_e import hermefit

x = np.array([1, 2, 3, 4])
y = np.array([-1, -2, -3, -4])
deg = 3
# using np.hermefit() method
gfg = hermefit(x, y, deg)

print(gfg)
```

**输出:**

> [6.52513495 e-15-1.00000000 e+00 3.34430164 e-15-4.02985428 e-16]

**例 2 :**

```py
# import numpy and hermefit
import numpy as np
from numpy.polynomial.hermite_e import hermefit

x = np.array([11, 22, 33, 44])
y = np.array([1, 2, 3, 4])
deg = 2
# using np.hermefit() method
gfg = hermefit(x, y, deg)

print(gfg)
```

**输出:**

> [-1.00370716 e-15 9.09090909 e-02-5.85610278 e-19]