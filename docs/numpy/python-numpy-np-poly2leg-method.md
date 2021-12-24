# Python | Numpy np.poly2leg()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-poly 2 leg-method/](https://www.geeksforgeeks.org/python-numpy-np-poly2leg-method/)

借助`**np.poly2leg()**`方法，我们可以从给定的多项式中得到勒让德级数系数。

> **语法:** `np.poly2leg(polynomial)`
> **返回:**返回勒让德级数的系数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.poly2leg()`方法，我们能够使用该方法从多项式中获得勒让德级数的系数。

```
# import numpy and poly2leg
import numpy as np
from numpy.polynomial.legendre import poly2leg

arr = np.array([0.1, 0.2, 0.3, 0.4, 0.5])
# using np.poly2leg() method
ans = poly2leg(arr)

print(ans)
```

**输出:**

> [ 0.3 0.44 0.48571429 0.16 0.11428571]

**例 2 :**

```
# import numpy and poly2leg
import numpy as np
from numpy.polynomial.legendre import poly2leg

arr = np.array([-0.5, -0.4, -0.3, -0.2, -0.1, 0, 0.1, 0.2, 0.3, 0.4, 0.5])
# using np.poly2leg() method
ans = poly2leg(arr)

print(ans)
```

**输出:**

> [-0.52692641-0.34424242 0.08651349 0.16149184 0.27684316 0.13948718
> 0.13127578 0.03905114 0.0295276 0.0042126 0.000422222]