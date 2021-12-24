# Python | Numpy np.poly2lag()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-poly 2 lag-method/](https://www.geeksforgeeks.org/python-numpy-np-poly2lag-method/)

借助于`**np.poly2lag()**`方法，我们可以从一个给定的多项式中得到拉盖尔级数系数。

> **语法:** `np.poly2lag(polynomial)`
> **返回:**返回拉盖尔级数的系数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.poly2lag()`方法，我们能够使用该方法从多项式中获得拉盖尔级数的系数。

```
# import numpy and poly2lag
import numpy as np
from numpy.polynomial.laguerre import poly2lag

arr = np.array([0.1, 0.2, 0.3, 0.4, 0.5])
# using np.poly2lag() method
ans = poly2lag(arr)

print(ans)
```

**输出:**

> [ 15.3 -56.6 79.8 -50.4 12\. ]

**例 2 :**

```
# import numpy and poly2lag
import numpy as np
from numpy.polynomial.laguerre import poly2lag

arr = np.array([-0.5, -0.4, -0.3, -0.2, -0.1, 0, 0.1, 0.2, 0.3, 0.4, 0.5])
# using np.poly2lag() method
ans = poly2lag(arr)

print(ans)
```

**输出:**

> [1.97272290 e+06-1.95546092 e+07 8.72343894 e+07-2.30634853 e+08
> 4.00196230 e+08-4.76216928 e+08 3.93562584 e+08-2.23051248 e+08
> 8.230512488