# Python | Numpy np.hermsub()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm sub-method/](https://www.geeksforgeeks.org/python-numpy-np-hermsub-method/)

借助`**np.hermsub()**`方法，我们可以用`np.hermsub()`方法将一个埃尔米特级数减去另一个埃尔米特级数。

> **语法:** `np.hermsub(series1, series2)`
> **返回:**返回级数相减后的系数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermsub()`方法，我们能够用这个方法得到两个 hermite 级数的减法。

```
# import numpy and hermsub
import numpy as np
from numpy.polynomial.hermite import hermsub

series1 = np.array([1, 2, 3, 4, 5])
series2 = np.array([6, 7, 8, 9, 10])

# using np.hermsub() method
gfg = hermsub(series1, series2)

print(gfg)
```

**输出:**

> [-5\. -5\. -5\. -5\. -5.]

**例 2 :**

```
# import numpy and hermsub
import numpy as np
from numpy.polynomial.hermite import hermsub

series1 = np.array([1, 0, 3, 0, 5])
series2 = np.array([0, 7, 0, 9, 0])

# using np.hermsub() method
gfg = hermsub(series1, series2)

print(gfg)
```

**输出:**

> [1\. -7\. 3\. -9\. 5.]