# Python | Numpy np.cheb2poly()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-cheb2poly-method/](https://www.geeksforgeeks.org/python-numpy-np-cheb2poly-method/)

借助`**np.cheb2poly()**`方法，我们可以利用`np.cheb2poly()`方法得到切比雪夫级数的多项式。

> **语法:** `np.cheb2poly(array)`
> **返回:**返回多项式系数数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.cheb2poly()`方法，我们能够使用该方法从切比雪夫级数中获得多项式。

```
# import numpy
import numpy as np
from numpy import polynomial as P

x = np.array([2, 5, 7])

# using np.cheb2poly() method
gfg = P.Chebyshev(x)
gfg = gfg.convert(kind = P.Polynomial)
gfg = P.chebyshev.cheb2poly(gfg)

print(gfg)
```

> [多项式([-5。, 5., 14.]，域=[-1。, 1.]，窗口=[-1。, 1.])]

**例 2 :**

```
# import numpy
import numpy as np
from numpy import polynomial as P

x = np.array([2, 3, 5, 7, 11])

# using np.cheb2poly() method
gfg = P.Chebyshev(x)
gfg = gfg.convert(kind = P.Polynomial)
gfg = P.chebyshev.cheb2poly(gfg)

print(gfg)
```

> [多项式([8。, -18., -78., 28., 88.]，域=[-1。, 1.]，窗口=[-1。, 1.])]