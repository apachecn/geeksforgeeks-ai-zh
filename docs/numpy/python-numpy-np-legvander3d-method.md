# Python | Numpy np.legvander3d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-legvander3d-method/](https://www.geeksforgeeks.org/python-numpy-np-legvander3d-method/)

`**np.legvander3d()**`方法用于返回度数 deg 和样本点 x、y、z 的范德蒙矩阵。

> **语法:** `np.legvander3d(x, y, z, deg)`
> **参数:**
> **x，y，z:**【Array _ like】点的数组。数据类型被转换为 float64 或 complex128，这取决于是否有任何元素是复杂的。如果 x 是标量，它被转换成一维数组。
> **度:**【int】所得矩阵的度。
> 
> **返回:**返回范德蒙矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.legvander3d()`方法，我们能够使用该方法获得伪范德蒙矩阵。

```py
# import numpy
import numpy as np
import numpy.polynomial.legendre as geek

# using np.legvander3d() method
ans = geek.legvander3d((1, 3, 5), (2, 4, 6), (1, 2, 3), [2, 2, 2])

print(ans)
```

**输出:**

> [[1.00000000 e+00 1.00000000 e+00 1.00000000 e+00
> 2.00000000 e+00 2.00000000 e+00 5.50000000 e+00
> 5.50000000 e+00 1.00000000 e+00 1.000000000 e+00 1.000000000 e+00 e+00
> 2.000000000 e+00 2.000000
> 1.00000000 e+00 3.00000000 e+00 1.30000000 e+01 6.00000000 e+00
> 1.800000000 e+01 5.350000000 e+01 1.60500000 e+02
> 6.95500000 e+02 5.00000000 e+00 1.50000000 e+01 6.50000000 e+01

**例 2 :**

```py
# import numpy
import numpy as np
import numpy.polynomial.legendre as geek

ans = geek.legvander3d((1, 2), (3, 4), (5, 6), [3, 3, 3])

print(ans)
```

**输出:**

> [1.00000000 e+00 5.00000000 e+00 3.700000000 e+01 3.05000000 e+02
> 3.00000000 e+00 1.50000000 e+01 1.11000000 e+02 9.15000000 e+02
> 1.30000000 e+01 6.50000000 e+01 4.8100 0000 e+02 3.96500000 e+03
> 6.30000000
> 【1.00000000 e+00 6.00000000 e+00 5.350000000 e+02
> 4.00000000 e+00 2.40000000 e+01 2.140000000 e+02 2.12400000 e+03
> 2.35000000 e+01 1.41000000 e+02 1.2505000 e+03 1.2475000 e+04