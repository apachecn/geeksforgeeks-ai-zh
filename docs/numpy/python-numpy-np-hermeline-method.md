# Python | Numpy np.hermeline()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermeline-method/](https://www.geeksforgeeks.org/python-numpy-np-hermeline-method/)

借助`**np.hermeline()**`方法，利用`np.hermeline()`方法可以得到 hermiteE 级数指定的直线。

> **语法:** `np.hermeline(off, scl)`
> **返回:**返回 hermiteE 系列为 **off + scl*x**

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermeline()`方法，我们能够通过使用这个方法得到 hermiteE 级数指定的直线。

```
# import numpy and hermeline
import numpy as np
from numpy.polynomial.hermite_e import hermeline

# using np.hermeline() method
gfg = hermeline(3, 4) + [1, 2]

print(gfg)
```

**输出:**

> [4 6]

**例 2 :**

```
# import numpy and hermeline
import numpy as np
from numpy.polynomial.hermite_e import hermeline

# using np.hermeline() method
gfg = hermeline(13, 4) + [10, 20]

print(gfg)
```

**输出:**

> [23 24]