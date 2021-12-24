# Python | Numpy np.hermzero()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm zero-method/](https://www.geeksforgeeks.org/python-numpy-np-hermzero-method/)

借助`**np.hermzero()**`方法，我们可以使用 **hermzero** 代替**NP . zero**使用`np.hermzero()`方法。

> **语法:** `np.hermzero()`
> **返回:**返回数组([0])

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermzero()`方法，我们能够获得与该方法相同的 np.zeros 的功能。

```py
# import numpy and hermzero
import numpy as np
from numpy.polynomial.hermite import hermzero

# using np.hermzero() method
gfg = hermzero + [1, 2, 3, 4, 5]

print(gfg)
```

**输出:**

> [1 2 3 4 5]

**例 2 :**

```py
# import numpy and hermzero
import numpy as np
from numpy.polynomial.hermite import hermzero

# using np.hermzero() method
gfg = hermzero + [[2, 4, 6], [3, 6, 9]]

print(gfg)
```

**输出:**

> [[2 4 6]
> [3 6 9]]