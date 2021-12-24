# Python | Numpy np.hermezero()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermezero-method/](https://www.geeksforgeeks.org/python-numpy-np-hermezero-method/)

借助`**np.hermezero()**`法，我们可以用 **hermezero** 代替`np.zeros()`用`np.hermezero()`法。

> **语法:** `np.hermezero`
> **返回:**返回零的数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermezero()`方法，我们能够获得与该方法相同的`np.zeros`功能。

```
# import numpy and hermezero
import numpy as np
from numpy.polynomial.hermite_e import hermezero

# using np.hermezero() method
gfg = hermezero + [1, 2, 3, 4, 5]

print(gfg)
```

**输出:**

> [1 2 3 4 5]

**例 2 :**

```
# import numpy and hermezero
import numpy as np
from numpy.polynomial.hermite_e import hermezero

# using np.hermezero() method
gfg = hermezero + [[2, 4, 6], [3, 6, 9]]

print(gfg)
```

**输出:**

> [[2 4 6]
> [3 6 9]]