# Python | Numpy np.chebadd()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-chebadd-method/](https://www.geeksforgeeks.org/python-numpy-np-chebadd-method/)

借助`**np.chebadd()**`方法，利用`np.chebadd()`方法可以得到两个**切比雪夫级数**的加法。

> **语法:** `np.chebadd(s1, s2)`
> **返回:**加法后返回一个数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.chebadd()`方法，我们能够使用该方法得到两个切比雪夫级数的加法。

```py
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (4, 6, 8)
s2 = (3, 5, 7)
# using np.chebadd() method
gfg = C.chebadd(s1, s2)

print(gfg)
```

**输出:**

> [ 7\. 11\. 15.]

**例 2 :**

```py
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (4, 6, 8, 1, 3, 5)
s2 = (3, 5, 7, 2, 4, 6)
# using np.chebadd() method
gfg = C.chebadd(s1, s2)

print(gfg)
```

**输出:**

> [ 7\. 11\. 15\. 3\. 7\. 11.]