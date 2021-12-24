# Python | Numpy NP . hermecompanion()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermecompanion-method/](https://www.geeksforgeeks.org/python-numpy-np-hermecompanion-method/)

借助`**np.hermecompanion()**`方法，利用`np.hermecompanion()`方法可以得到 hermiteE 级数的伴矩阵。

> **语法:** `np.hermecompanion(series)`
> **返回:**返回同伴矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermecompanion()`方法，我们能够使用该方法从 hermiteE 系列中获得伴随矩阵。

```
# import numpy and hermecompanion
import numpy as np
from numpy.polynomial.hermite_e import hermecompanion

series = np.array([6, 7, 8, 9, 10])
# using np.hermecompanion() method
gfg = hermecompanion(series)

print(gfg)
```

**输出:**

> [[ 0.1.0.-0.24494897]
> 【1。0.1.41421356-0.2857738]
> 【0。1.41421356 0.1.27017059]
> 【0。0.1.73205081 -0.9 ]]

**例 2 :**

```
# import numpy and hermecompanion
import numpy as np
from numpy.polynomial.hermite_e import hermecompanion

series = np.array([1, 2, 3, 4, 5])
# using np.hermecompanion() method
gfg = hermecompanion(series)

print(gfg)
```

**输出:**

> [[ 0.1.0.-0.08164966]
> 【1。0.1.41421356-0.16329932]
> 【0。1.41421356 0.1.38564065]
> 【0。0.1.73205081 -0.8 ]]