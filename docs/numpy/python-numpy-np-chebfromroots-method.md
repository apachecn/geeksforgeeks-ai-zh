# Python | Numpy NP . chebfromnroot()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-NP-chebfromnroot-method/](https://www.geeksforgeeks.org/python-numpy-np-chebfromroots-method/)

借助`**np.chebfromroots()**`方法，我们可以得到`np.chebfromroots()`方法中以根为参数传递的切比雪夫级数。

> **语法:** `np.chebfromroots(roots)`
> **返回:**返回切比雪夫系列。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.chebfromroots()`方法，我们能够获得由通过参数传递的根生成的切比雪夫级数。

```py
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebfromroots() method
gfg = cheb.chebfromroots((2, 4, 8, 1))

print(gfg)
```

**输出:**

> [9.9375 e+01-1.3125 e+02 3.5500 e+01-3.7500 e+00 1.2500 e-01]

**例 2 :**

```py
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebfromroots() method
gfg = cheb.chebfromroots((-3, 4, -5, 1, 10))

print(gfg)
```

**输出:**

> [-5.19125 e+02 4.52375 e+02 8.00000 e+01-1.24375 e+01-8.75000 e-01 6.25000 e-02]