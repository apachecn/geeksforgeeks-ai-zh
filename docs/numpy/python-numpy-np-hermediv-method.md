# Python | Numpy np.hermediv()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermediv-method/](https://www.geeksforgeeks.org/python-numpy-np-hermediv-method/)

借助`**np.hermediv()**`方法，利用`np.hermediv()`方法可以得到两个 hermiteE 级数的除法。

> **语法:** `np.hermediv(series1, series2)`
> **返回:**返回两个 hermiteE 系列的划分。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermediv()`方法，我们能够利用这个方法得到两个 hermiteE 级数的除法。

```
# import numpy and hermediv
import numpy as np
from numpy.polynomial.hermite_e import hermediv

series1 = np.array([1, 2, 3, 4])
series2 = np.array([10, 11, 12, 13])

# using np.hermediv() method
gfg = hermediv(series1, series2)

print(gfg)
```

**输出:**

> (数组([0.30769231])，数组([-2.07692308，-1.38461538，-0.69230769])

**例 2 :**

```
# import numpy and hermediv
import numpy as np
from numpy.polynomial.hermite_e import hermediv

series1 = np.array([11, 22, 33, 44])
series2 = np.array([10, 11, 12, 13])

# using np.hermediv() method
gfg = hermediv(series1, series2)

print(gfg)
```

**输出:**

> (数组([3.38461538])，数组([-22.84615385，-15.23076923，-7.61538462])