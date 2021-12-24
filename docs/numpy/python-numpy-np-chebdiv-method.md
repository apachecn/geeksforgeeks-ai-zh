# Python | Numpy np.chebdiv()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-NP-chebdiv-method/

借助`**np.chebdiv()**`方法，利用`np.chebdiv()`方法可以得到两个**切比雪夫级数**的除法。

> **语法:** `np.chebdiv(s1, s2)`
> **归:**师后归阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.chebdiv()`方法，我们能够使用该方法获得两个切比雪夫级数的除法。

```py
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (4, 6, 8)
s2 = (3, 5, 7)

# using np.chebdiv() method
gfg = C.chebdiv(s1, s2)

print(gfg)
```

**输出:**

> (数组([1.14285714])，数组([0.57142857，0.28571429])

**例 2 :**

```py
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (4, 6, 8, 1, 3, 5)
s2 = (3, 5, 7, 2, 4, 6)
# using np.chebdiv() method
gfg = C.chebdiv(s1, s2)

print(gfg)
```

**输出:**

> (array([0.833333333])，array([ 1.5，1.83333333，2.16666667，-0.666667，-0.333333333])