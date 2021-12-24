# Python | Numpy np.mapparms()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-mapparms-method/](https://www.geeksforgeeks.org/python-numpy-np-mapparms-method/)

借助`**np.mapparms()**`方法，我们可以利用`np.mapparms()`方法得到域之间的线性映射参数。

> **语法:** `np.mapparms(old, new)`
> **返回:**返回线性地图的参数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.mapparms()`方法，我们能够使用该方法获得参数的线性映射。

```
# import numpy and mapparms
import numpy as np
from numpy.polynomial import polyutils as pu

# using np.mapparms() method
gfg = pu.mapparms([1, 2, 3], [5, -5])

print(gfg)
```

**输出:**

> (15.0, -10.0)

**例 2 :**

```
# import numpy and mapparms
import numpy as np
from numpy.polynomial import polyutils as pu

# using np.mapparms() method
gfg = pu.mapparms([1, 2, 3, 4, 5, 6], [5, 15])

print(gfg)
```

**输出:**

> (-5.0, 10.0)