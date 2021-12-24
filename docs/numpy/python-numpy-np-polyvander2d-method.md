# Python | Numpy np.polyvander2d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-polyvander2d-method/](https://www.geeksforgeeks.org/python-numpy-np-polyvander2d-method/)

借助于`**np.polyvander2d()**`方法，我们可以从给定的数组中得到伪范德蒙矩阵，通过`np.polyvander2d()`方法将该矩阵作为参数传递。

> **语法:** `np.polyvander2d(x, y, deg)`
> **参数:**
> **x，y:**【Array _ like】点的数组。数据类型被转换为 float64 或 complex128，这取决于是否有任何元素是复杂的。如果 x 是标量，它被转换成一维数组
> **度:**【int】所得矩阵的度数。
> 
> **返回:**返回具有大小即 array.size +(度+ 1)的矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.polyvander2d()`方法，我们能够使用该方法获得伪范德蒙矩阵。

```py
# import numpy
import numpy as np
import numpy.polynomial.polynomial as geek

# using np.polyvander() method
ans = geek.polyvander2d((1, 3, 5, 7), (2, 4, 6, 8), [2, 2])

print(ans)
```

**输出:**

> [[1.00000000 e+00 2.00000000 e+00 4.00000000 e+00 1.00000000 e+00
> 2.0000000000 e+00 4.000000000 e+00 1.00000000 e+00 2.000000000 e+00
> 4.00000000000000 e+00]

**例 2 :**

```py
# import numpy
import numpy as np
import numpy.polynomial.polynomial as geek

ans = geek.polyvander2d((1, 2, 3, 4), (5, 6, 7, 8), [3, 3])

print(ans)
```

**输出:**

> [1.00000000 e+00 5.00000000 e+00 2.50000000 e+01 1.250000000 e+02
> 1.00000000 e+00 5.00000000 e+00 2.50000000 e+01 1.250000000 e+02
> 1.00000000 e+00 5.00000000 e+00 2.50000000 e+01 1.250000000 e+02
> 1.00000000 e+00