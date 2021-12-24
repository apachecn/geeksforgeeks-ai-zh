# Python | Numpy np.hermx()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-np-hermx-method/](https://www.geeksforgeeks.org/python-numpy-np-hermx-method/)

借助`**np.hermx()**`方法，利用`np.hermx()`方法可以得到 hermite 级数中具有值**数组(【0，0.5】)**的滤波器。

> **语法:** `np.hermx`
> **返回:**返回数组的过滤器([0，0.5])

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermx()`方法，我们能够使用该方法获得埃尔米特级数中的**数组(【0，0.5】)**的过滤器。

```
# import numpy and hermx
import numpy as np
from numpy.polynomial.hermite import hermx

# using np.hermx() method
for i in range(5):
    gfg = hermx + [i, i + 1]
    print(gfg)
```

**输出:**

> [0.1.5]
> 【1。2.5]
> 【2。3.5】
> 【3。4.5]
> 【4。5.5]

**例 2 :**

```
# import numpy and hermx
import numpy as np
from numpy.polynomial.hermite import hermx

# using np.hermx() method
for i in range(5):
    gfg = hermx + [i-1, i + 1]
    print(gfg)
```

**输出:**

> [-1.1.5]
> 【0。2.5]
> 【1。3.5】
> 【2。4.5]
> 【3。5.5]