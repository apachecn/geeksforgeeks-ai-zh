# Python | Numpy np.hermone()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermone-method/](https://www.geeksforgeeks.org/python-numpy-np-hermone-method/)

借助`**np.hermone()**`法，我们可以用 **hermzero** 代替**NP . one**用`np.hermone()`法。

> **语法:** `np.hermone()`
> **返回:**返回数组([1])

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermone()`方法，我们能够获得与该方法相同的 np.ones 的功能。

```
# import numpy and hermone
import numpy as np
from numpy.polynomial.hermite import hermone

# using np.hermone() method
gfg = hermone + [1, 2, 3, 4, 5]

print(gfg)
```

**输出:**

> [2 3 4 5 6]

**例 2 :**

```
# import numpy and hermone
import numpy as np
from numpy.polynomial.hermite import hermone

# using np.hermone() method
gfg = hermone + [[2, 4, 6], [3, 6, 9]]

print(gfg)
```

**输出:**

> [[ 3 5 7]
> [ 4 7 10]]