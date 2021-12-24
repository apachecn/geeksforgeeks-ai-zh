# Python | Numpy np.polyvander3d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-polyvander3d-method/](https://www.geeksforgeeks.org/python-numpy-np-polyvander3d-method/)

`**np.polyvander3d()**`方法用于返回度数 deg 和样本点 x、y、z 的范德蒙矩阵。

> **语法:** `np.polyvander3d(x, y, z, deg)`
> **参数:**
> **x，y，z:**【Array _ like】点的数组。数据类型被转换为 float64 或 complex128，这取决于是否有任何元素是复杂的。如果 x 是标量，它被转换成一维数组。
> **度:**【int】所得矩阵的度。
> 
> **返回:**返回范德蒙矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.polyvander3d()`方法，我们能够使用该方法获得伪范德蒙矩阵。

```
# import numpy
import numpy as np
import numpy.polynomial.polynomial as geek

# using np.polyvander3d() method
ans = geek.polyvander3d((1, 3, 5), (2, 4, 6), (1, 2, 3), [2, 2, 2])

print(ans)
```

**输出:**

> [[1.00000000 e+00 1.00000000 e+00 2.00000000 e+00
> 2.00000000 e+00 2.00000000 e+00 4.00000000 e+00 4.00000000 e+00
> 4.00000000 e+00 1.00000000 e+00 1.000000000 e+00 1.000000000 e+00 e+00
> 2.00000000 e+00 e
> 1.00000000 e+00 3.00000000 e+00 9.00000000 e+00 6.00000000 e+00
> 1.800000000 e+01 5.40000000 e+01 3.6000000 e+01 1.080000000 e+02
> 3.24000 00000 e+02 5.000000000 e+00 1.50000000 e+01 4.50000000 e+01

**例 2 :**

```
# import numpy
import numpy as np
import numpy.polynomial.polynomial as geek

ans = geek.polyvander3d((1, 2), (3, 4), (5, 6), [3, 3, 3])

print(ans)
```

**输出:**

> [[1.00000000 e+00 5.00000000 e+00 2.50000000 e+01 1.250000000 e+00 1.50000000 e+01 7.50000000 e+01 3.750000000 e+02
> 9.00000000 e+00 4.50000000 e+01 2.250000000 e+02 1.12500000 e+03
> 2.700000000
> 【1.00000000 e+00 6.00000000 e+00 3.6000000 e+01 2.16000000 e+02
> 4.00000000 e+00 2.40000000 e+01 1.44000000 e+02 8.64000000 e+02
> 1.6000000 e+01 9.6000000 e+01 5.76000000 e+02 3.45600000 e+03