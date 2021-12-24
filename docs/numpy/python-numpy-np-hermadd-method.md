# Python | Numpy np.hermadd()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermadd-method/](https://www.geeksforgeeks.org/python-numpy-np-hermadd-method/)

借助`**np.hermadd()**`方法，我们可以用`np.hermadd()`方法将一个埃尔米特级数加到另一个埃尔米特级数上。

> **语法:** `np.hermadd(series1, series2)`
> **返回:**返回级数相加后的系数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermadd()`方法，我们能够通过使用这个方法得到两个 hermite 级数的加法。

```
# import numpy and hermadd
import numpy as np
from numpy.polynomial.hermite import hermadd

series1 = np.array([1, 2, 3, 4, 5])
series2 = np.array([6, 7, 8, 9, 10])

# using np.hermadd() method
gfg = hermadd(series1, series2)

print(gfg)
```

**输出:**

> [7\. 9\. 11\. 13\. 15.]

**例 2 :**

```
# import numpy and hermadd
import numpy as np
from numpy.polynomial.hermite import hermadd

series1 = np.array([1, 0, 3, 0, 5])
series2 = np.array([0, 7, 0, 9, 0])

# using np.hermadd() method
gfg = hermadd(series1, series2)

print(gfg)
```

**输出:**

> [1\. 7\. 3\. 9\. 5.]