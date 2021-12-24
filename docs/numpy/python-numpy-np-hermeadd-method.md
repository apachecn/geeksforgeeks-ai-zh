# Python | Numpy NP . hermadd()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermad-method/](https://www.geeksforgeeks.org/python-numpy-np-hermeadd-method/)

借助`**np.hermeadd()**`方法，利用`np.hermeadd()`方法可以得到两个 hermiteE 级数的加法。

> **语法:** `np.hermeadd(series1, series2)`
> **返回:**返回两个 hermiteE 系列的加法。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermeadd()`方法，我们能够通过使用这个方法得到两个 hermiteE 级数的加法。

```py
# import numpy and hermeadd
import numpy as np
from numpy.polynomial.hermite_e import hermeadd

series1 = np.array([1, 2, 3, 4])
series2 = np.array([10, 11, 12, 13])

# using np.hermeadd() method
gfg = hermeadd(series1, series2)

print(gfg)
```

**输出:**

> [11\. 13\. 15\. 17.]

**例 2 :**

```py
# import numpy and hermeadd
import numpy as np
from numpy.polynomial.hermite_e import hermeadd

series1 = np.array([11, 22, 33, 44])
series2 = np.array([10, 11, 12, 13])

# using np.hermeadd() method
gfg = hermeadd(series1, series2)

print(gfg)
```

**输出:**

> [21\. 33\. 45\. 57.]