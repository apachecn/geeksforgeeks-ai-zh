# Python | Numpy np.ma.mini()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-ma-mini-method/](https://www.geeksforgeeks.org/python-numpy-np-ma-mini-method/)

借助`**np.ma.mini()**`方法，我们可以利用`np.ma.mini()`方法得到掩蔽数组的最小值。

> **语法:** `np.ma.mini()`
> **返回:**返回屏蔽阵的最小值。

**示例#1 :**
在这个示例中我们可以看到，通过使用`np.ma.mini()`方法，我们能够通过使用该方法来获得掩码数组的最小值。

```
# import numpy
import numpy as np
import numpy.ma as ma

# using np.ma.mini() method
gfg = ma.array(np.arange(6), mask =[-2, -1, 0, 1, 2, 3]).reshape(3, 2)
min = gfg.mini()

print(min)
```

**输出:**

> Two

**例 2 :**

```
# import numpy
import numpy as np
import numpy.ma as ma

# using np.ma.mini() method
gfg = ma.array(np.arange(10), mask =[-2, -1, 0, 1, 0, 3, 0, 0, 0, 0]).reshape(2, 5)
min = gfg.mini()

print(min)
```

**输出:**

> Two