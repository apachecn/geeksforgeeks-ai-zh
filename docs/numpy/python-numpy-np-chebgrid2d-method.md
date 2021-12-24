# Python | Numpy np.chebgrid2d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-chebgrid2d-method/](https://www.geeksforgeeks.org/python-numpy-np-chebgrid2d-method/)

借助`**np.chebgrid2d()**`方法，利用`np.chebgrid2d()`方法对 x 和 y 的笛卡尔积上的切比雪夫级数求值后，可以得到系数的数组。

> **语法:** `np.chebgrid2d(x, y, c)`
> **返回:**在(x，y)上求值后返回数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.chebgrid2d()`方法，我们能够通过评估 x 和 y 的笛卡尔乘积上的切比雪夫级数来获得系数数组。

```py
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebgrid2d() method
gfg = cheb.chebgrid2d((2, 5), (1, 3), (2, -4, 1))

print(gfg)
```

**输出:**

> [32\. 94.]

**例 2 :**

```py
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebgrid2d() method
gfg = cheb.chebgrid2d((1, 3, 5, 7), (2, 4, 8), (2, -4, 1, 5, 1))

print(gfg)
```

**输出:**

> [719680\. 6486180\. 52831708.]