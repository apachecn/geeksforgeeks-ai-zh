# Python | Numpy np.hermmulx()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-NP-herm mulx-method/](https://www.geeksforgeeks.org/python-numpy-np-hermmulx-method/)

借助`**np.hermmulx()**`方法，我们可以利用`np.hermmulx()`方法得到 hermite 级数与 x 的乘积，其中 x 为自变量。

> **语法:** `np.hermmulx(series)`
> **返回:**返回级数相乘后的系数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermmulx()`方法，我们能够用这个方法得到埃尔米特级数与自变量 x 相乘后的级数系数。

```
# import numpy and hermmulx
import numpy as np
from numpy.polynomial.hermite import hermmulx

series = np.array([6, 7, 8, 9, 10])

# using np.hermmulx() method
gfg = hermmulx(series)

print(gfg)
```

**输出:**

> [7\. 19\. 30.5 44\. 4.5 5.]

**例 2 :**

```
# import numpy and hermmulx
import numpy as np
from numpy.polynomial.hermite import hermmulx

series = np.array([1, 2, 3])

# using np.hermmulx() method
gfg = hermmulx(series)

print(gfg)
```

**输出:**

> [2\. 6.5 1\. 1.5]