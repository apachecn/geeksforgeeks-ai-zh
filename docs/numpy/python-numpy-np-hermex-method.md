# Python | Numpy np.hermex()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermex-method/](https://www.geeksforgeeks.org/python-numpy-np-hermex-method/)

借助`**np.hermex()**`方法，利用`np.hermex()`方法可以得到 hermiteE 级数中具有值**数组(【0，1】)**的滤波器。

> **语法:** `np.hermex`
> **返回:**返回数组的过滤器([0，1])

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermex()`方法，我们能够使用该方法获得 hermiteE 系列中的**数组(【0，1】)**的过滤器。

```py
# import numpy and hermex
import numpy as np
from numpy.polynomial.hermite_e import hermex

# using np.hermex() method
for i in range(5):
    gfg = hermex + [i, i + 1]
    print(gfg)
```

**输出:**

> [0 2]
> 【1 3】
> 【2 4】
> 【3 5】
> 【4 6】

**例 2 :**

```py
# import numpy and hermex
import numpy as np
from numpy.polynomial.hermite_e import hermex

# using np.hermex() method
for i in range(5):
    gfg = hermex + [i-1, i + 1]
    print(gfg)
```

**输出:**

> [-1 2]
> 【0 3】
> 【1 4】
> 【2 5】
> 【3 6】