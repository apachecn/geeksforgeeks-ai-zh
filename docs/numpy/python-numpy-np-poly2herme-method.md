# Python | Numpy np.poly2herme()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-poly 2 herme-method/](https://www.geeksforgeeks.org/python-numpy-np-poly2herme-method/)

借助`**np.poly2herme()**`方法，利用`np.poly2herme()`方法可以由多项式得到 hermiteE 级数。

> **语法:** `np.poly2herme(series)`
> **返回:**返回 hermiteE 级数的系数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.poly2herme()`方法，我们能够使用该方法从多项式中获得 hermiteE 级数的系数。

```py
# import numpy and poly2herme
import numpy as np
from numpy.polynomial.hermite_e import poly2herme

x = np.array([0.1, 0.2, 0.3, 0.4])
# using np.poly2herme() method
gfg = poly2herme(x)

print(gfg)
```

**输出:**

> [0.4 1.4 0.3 0.4]

**例 2 :**

```py
# import numpy and poly2herme
import numpy as np
from numpy.polynomial.hermite_e import poly2herme

x = np.array([-0.5, -0.4, -0.3, -0.2, -0.1, 0, 0.4, 0.5])
# using np.poly2herme() method
gfg = poly2herme(x)

print(gfg)
```

**输出:**

> [ 4.9 51.5 17.1 52.3 5.9 10.5 0.4 0.5]