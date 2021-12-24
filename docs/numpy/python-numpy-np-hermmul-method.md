# Python | Numpy np.hermmul()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-NP-herm mul-method/](https://www.geeksforgeeks.org/python-numpy-np-hermmul-method/)

借助`**np.hermmul()**`方法，利用`np.hermmul()`方法可以得到两个厄米级数的乘积。

> **语法:** `np.hermmul(series1, series2)`
> **返回:**返回级数相乘后的系数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermmul()`方法，我们能够用这个方法得到两个 hermite 级数相乘后的级数系数。

```py
# import numpy and hermmul
import numpy as np
from numpy.polynomial.hermite import hermmul

series1 = np.array([1, 2, 3, 4, 5])
series2 = np.array([6, 7, 8, 9, 10])

# using np.hermmul() method
gfg = hermmul(series1, series2)

print(gfg)
```

**输出:**

> [21154\. 17903\. 44860\. 13458\. 16278\. 2154\. 1706\. 85\. 50.]

**例 2 :**

```py
# import numpy and hermmul
import numpy as np
from numpy.polynomial.hermite import hermmul

series1 = np.array([1, 2, 3])
series2 = np.array([1, 2, 3])

# using np.hermmul() method
gfg = hermmul(series1, series2)

print(gfg)
```

**输出:**

> [81\. 52\. 82\. 12\. 9.]