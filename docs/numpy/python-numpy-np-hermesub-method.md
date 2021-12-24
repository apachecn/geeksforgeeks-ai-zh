# Python | Numpy np.hermesub()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermesub-method/](https://www.geeksforgeeks.org/python-numpy-np-hermesub-method/)

借助`**np.hermesub()**`方法，利用`np.hermesub()`方法可以得到两个 hermiteE 级数的减法。

> **语法:** `np.hermesub(series1, series2)`
> **返回:**返回两个 hermiteE 级数的减法。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermesub()`方法，我们能够用这个方法得到两个 hermiteE 级数的减法。

```
# import numpy and hermesub
import numpy as np
from numpy.polynomial.hermite_e import hermesub

series1 = np.array([1, 2, 3, 4])
series2 = np.array([10, 11, 12, 13])

# using np.hermesub() method
gfg = hermesub(series1, series2)

print(gfg)
```

**输出:**

> [-9\. -9\. -9\. -9.]

**例 2 :**

```
# import numpy and hermesub
import numpy as np
from numpy.polynomial.hermite_e import hermesub

series1 = np.array([11, 22, 33, 44])
series2 = np.array([10, 11, 12, 13])

# using np.hermesub() method
gfg = hermesub(series1, series2)

print(gfg)
```

**输出:**

> [ 1\. 11\. 21\. 31.]