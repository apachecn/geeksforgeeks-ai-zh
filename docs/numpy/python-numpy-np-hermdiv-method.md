# Python | Numpy np.hermdiv()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm div-method/](https://www.geeksforgeeks.org/python-numpy-np-hermdiv-method/)

借助`**np.hermdiv()**`方法，利用`np.hermdiv()`方法可以得到两个厄米级数的除法。

> **语法:** `np.hermdiv(series1, series2)`
> **返回:**返回除法后的级数系数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermdiv()`方法，我们能够用这个方法得到两个 hermite 级数除后的级数系数。

```
# import numpy and hermdiv
import numpy as np
from numpy.polynomial.hermite import hermdiv

series1 = np.array([1, 2, 3, 4, 5])
series2 = np.array([6, 7, 8, 9, 10])

# using np.hermdiv() method
gfg = hermdiv(series1, series2)

print(gfg)
```

**输出:**

> (数组([0.5])，数组([-2。, -1.5, -1., -0.5]))

**例 2 :**

```
# import numpy and hermdiv
import numpy as np
from numpy.polynomial.hermite import hermdiv

series1 = np.array([1, 2, 3])
series2 = np.array([1, 2, 3])

# using np.hermdiv() method
gfg = hermdiv(series1, series2)

print(gfg)
```

**输出:**

> (数组([1。])，数组([0。]))