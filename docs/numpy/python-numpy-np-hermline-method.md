# Python | Numpy np.hermline()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm line-method/](https://www.geeksforgeeks.org/python-numpy-np-hermline-method/)

借助`**np.hermline()**`方法，利用`np.hermline()`方法可以得到埃尔米特级数指定的直线。

> **语法:** `np.hermline(off, scl)`
> **返回:**返回厄米系列为 **off + scl*x**

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermline()`方法，我们能够通过使用这个方法得到埃尔米特级数指定的直线。

```
# import numpy and hermline
import numpy as np
from numpy.polynomial.hermite import hermline

# using np.hermline() method
gfg = hermline(3, 4) + [1, 2]

print(gfg)
```

**输出:**

> [4\. 4.]

**例 2 :**

```
# import numpy and hermline
import numpy as np
from numpy.polynomial.hermite import hermline

# using np.hermline() method
gfg = hermline(13, 4) + [10, 20]

print(gfg)
```

**输出:**

> [23\. 22.]