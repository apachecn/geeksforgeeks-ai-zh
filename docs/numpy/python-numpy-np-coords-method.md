# Python | Numpy np.coords()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-coords-method/](https://www.geeksforgeeks.org/python-numpy-np-coords-method/)

借助`**np.coords()**`方法，我们可以使用`np.coords()`方法在迭代中获得下一个值的坐标。

> **语法:** `np.coords()`
> **返回:**返回下一个迭代器的坐标。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.coords()`方法，我们能够使用该方法获得下一个迭代器的坐标。

```
# import numpy
import numpy as np

a = np.array([1, 2, 3])
# using np.coords() method
gfg = a.flat
next(gfg)
print(gfg.coords)
```

**输出:**

> (1, )

**例 2 :**

```
# import numpy
import numpy as np

a = np.array([[1, 2, 3], [4, 5, 6]])
# using np.coords() method
gfg = a.flat
next(gfg)
next(gfg)
next(gfg)
next(gfg)
print(gfg.coords)
```

**输出:**

> (1, 1)