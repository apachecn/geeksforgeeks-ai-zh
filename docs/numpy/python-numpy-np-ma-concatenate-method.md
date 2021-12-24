# Python | Numpy NP . ma . concatenate()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-ma-concatenate-method/](https://www.geeksforgeeks.org/python-numpy-np-ma-concatenate-method/)

借助`**np.ma.concatenate()**`方法，我们可以借助`np.ma.concatenate()`方法将两个数组串联起来。

> **语法:** `np.ma.concatenate([list1, list2])`
> **返回:**串联后返回数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.ma.concatenate()`方法，我们能够在该方法的帮助下获得连接数组。

```
# import numpy
import numpy as np
import numpy.ma as ma

gfg1 = np.array([1, 2, 3])
gfg2 = np.array([4, 5, 6])

# using np.ma.concatenate() method
gfg = ma.concatenate([gfg1, gfg2])

print(gfg)
```

**输出:**

> [1 2 3 4 5 6]

**例 2 :**

```
# import numpy
import numpy as np
import numpy.ma as ma

gfg1 = np.array([11, 22, 33])
gfg2 = np.array([41, 52, 63])

# using np.ma.concatenate() method
gfg = ma.concatenate([[gfg1], [gfg2]])

print(gfg)
```

**输出:**

> [[11 22 33]
> [41 52 63]]