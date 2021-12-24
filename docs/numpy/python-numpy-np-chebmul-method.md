# Python | Numpy np.chebmul()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-chebmul-method/](https://www.geeksforgeeks.org/python-numpy-np-chebmul-method/)

借助`**np.chebmul()**`方法，利用`np.chebmul()`方法可以得到两个**切比雪夫级数**的乘积。

> **语法:** `np.chebmul(s1, s2)`
> **返回:**乘法后返回一个数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.chebmul()`方法，我们能够使用该方法获得两个切比雪夫级数的乘法。

```py
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (4, 6, 8)
s2 = (3, 5, 7)
# using np.chebmul() method
gfg = C.chebmul(s1, s2)

print(gfg)
```

**输出:**

> [55\. 79\. 67\. 41\. 28.]

**例 2 :**

```py
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (4, 6, 8, 1, 3, 5)
s2 = (3, 5, 7, 2, 4, 6)
# using np.chebmul() method
gfg = C.chebmul(s1, s2)

print(gfg)
```

**输出:**

> [ 77\. 114.5 110\. 113\. 92\. 70\. 58\. 46.5 14\. 19\. 15\. ]