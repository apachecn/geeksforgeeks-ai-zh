# Python | Numpy np.hermfit()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm fit-method/](https://www.geeksforgeeks.org/python-numpy-np-hermfit-method/)

借助`**np.hermfit()**`方法，利用`np.hermfit()`方法可以得到埃尔米特级数的最小二乘拟合。

> **语法:** `np.hermfit(x, y, deg)`
> **返回:**返回埃尔米特级数的最小二乘拟合。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermfit()`方法，我们能够通过使用该方法来获得给定数据的埃尔米特级数的最小二乘拟合。

```py
# import numpy and hermfit
import numpy as np
from numpy.polynomial.hermite import hermfit

x = np.array([-3, -2, -1])
y = np.array([1, 2, 3])
deg = 2

# using np.hermfit() method
gfg = hermfit(x, y, deg)

print(gfg)
```

**输出:**

> [4.00000000 e+00 5.0000000 e-01 1.56777498 e-16]

**例 2 :**

```py
# import numpy and hermfit
import numpy as np
from numpy.polynomial.hermite import hermfit

x = np.array([-2, -1, 0, 1, 2])
y = np.array([0.1, 0.2, 0.3, 0.4, 0.5])
deg = 3

# using np.hermfit() method
gfg = hermfit(x, y, deg)

print(gfg)
```

**输出:**

> [3.00000000 e-01 5.00000000 e-02 2.76178300 e-18-1.46465661 e-18]