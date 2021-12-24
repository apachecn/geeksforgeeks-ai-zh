# Python | Numpy np.chebgrid3d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-chebgrid3d-method/](https://www.geeksforgeeks.org/python-numpy-np-chebgrid3d-method/)

借助`**np.chebgrid3d()**`方法，我们可以通过`np.chebgrid3d()`方法对 x，y，z 的笛卡尔积上的切比雪夫级数求值后得到系数的数组。

> **语法:** `np.chebgrid3d(x, y, z, c)`
> **返回:**在(x，y，z)上求值后返回数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.chebgrid3d()`方法，我们能够通过评估 x、y 和 z 的笛卡尔乘积上的切比雪夫级数来获得系数数组。

```
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebgrid3d() method
gfg = cheb.chebgrid3d((2, 5), (1, 3), (5, 6, -3), (2, -4, 1))

print(gfg)
```

**输出:**

> [502\. 596\. -250.]

**例 2 :**

```
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebgrid3d() method
gfg = cheb.chebgrid3d((1, -3, 7), (-2, 4, -8), (3, -4, 1), (2, -4, 1, 5, 1))

print(gfg)
```

**输出:**

> [57913404\. 97926342\. 4230432.]