# Python | Numpy np.chebsub()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-cheb sub-method/](https://www.geeksforgeeks.org/python-numpy-np-chebsub-method/)

借助`**np.chebsub()**`方法，利用`np.chebsub()`方法可以得到两个**切比雪夫级数**的减法。

> **语法:** `np.chebsub(s1, s2)`
> **返回:**减法后返回一个数组。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.chebsub()`方法，我们能够用这个方法得到两个切比雪夫级数的减法。

```
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (4, 6, 8)
s2 = (3, 5, 7)
# using np.chebsub() method
gfg = C.chebsub(s1, s2)

print(gfg)
```

**输出:**

> [1., 1., 1.]

**例 2 :**

```
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (4, 6, 8, 1, 3, 5)
s2 = (3, 5, 7, 2, 4, 6)
# using np.chebsub() method
gfg = C.chebsub(s1, s2)

print(gfg)
```

**输出:**

> [ 1\. 1\. 1\. -1\. -1\. -1.]