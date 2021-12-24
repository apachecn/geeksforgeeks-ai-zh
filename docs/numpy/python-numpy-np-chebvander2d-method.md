# Python | Numpy NP . chebvandr2d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-chebvander2d-method/](https://www.geeksforgeeks.org/python-numpy-np-chebvander2d-method/)

借助于`**np.chebvander2d()**`方法，我们可以从给定的数组中得到伪范德蒙 2D 矩阵，用`np.chebvander2d()`方法将该矩阵作为参数传递。

> **语法:** `np.chebvander2d(x, y, degree)`
> **返回:**返回大小为 array.size +(度+ 1)的 2D 矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.chebvander2d()`方法，我们能够使用该方法获得伪范德蒙 2D 矩阵。

```
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebvander2d() method
gfg = cheb.chebvander2d((2, 4, 8, 1), (2, 4, 8, 1), 2)

print(gfg)
```

**输出:**

> [[ 1.2.7.】
> 【1。4.31.】
> 【1。8.127.】
> 【1。1.1.]]

**例 2 :**

```
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebvander2d() method
gfg = cheb.chebvander2d((3, 5, 1, 10), (3, 5, 1, 10), 4)

print(gfg)
```

**输出:**

> 【【1.0000 e+00 3.0000 e+00 1.7000 e+01 9.9000 e+01 5.7700 e+02】
> 【1.0000 e+00 5.0000 e+00 4.9000 e+01 4.8500 e+02 4.8010 e+03】
> 【1.0000 e+00 1.00000 e+00 1.00000 e】