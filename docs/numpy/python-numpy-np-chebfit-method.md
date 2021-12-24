# Python | Numpy np.chebfit()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-chebfit-method/](https://www.geeksforgeeks.org/python-numpy-np-chebfit-method/)

借助`**np.chebfit()**`方法，利用`np.chebfit()`方法可以得到切比雪夫级数的最小二乘拟合。

> **语法:** `np.chebfit(x, y, degree)`
> **返回:**返回数组的切比雪夫级数系数值。

**示例#1 :**
在这个示例中，我们可以看到，使用`np.chebfit()`方法，我们能够使用该方法获得切比雪夫级数的最小二乘拟合。

```py
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebfit() method
gfg = cheb.chebfit((4, -5), (5, 7), 1)

print(gfg)
```

**输出:**

> [5.88888889, -0.22222222]

**例 2 :**

```py
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebfit() method
gfg = cheb.chebfit((-3, 4, 10), (1, 2, 3), 3)

print(gfg)
```

**输出:**

> [1.39458146 e+00 1.41166773 e-01 1.53673202 e-03-2.82264138 e-05]