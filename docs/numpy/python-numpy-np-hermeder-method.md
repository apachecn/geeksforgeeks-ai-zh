# python | num py NP . hermer()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermeder-method/](https://www.geeksforgeeks.org/python-numpy-np-hermeder-method/)

借助`**np.hermeder()**`方法，我们可以用`np.hermeder()`方法来判别 hermiteE 级数。

> **语法:** `np.hermeder(series, m)`
> 
> **返回:**返回微分级数的系数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermeder()`方法，我们能够利用这个方法得到 hermiteE 级数的微分级数系数。

```
# import numpy and harmeder
import numpy as np
from numpy.polynomial.hermite_e import hermeder

series = np.array([2, 0.3, 4, 0.5, 6])

# using np.harmeder() method
gfg = hermeder(series, m = 2)

print(gfg)
```

**输出:**

> [8\. 3\. 72.]

**例 2 :**

```
# import numpy and harmeder
import numpy as np
from numpy.polynomial.hermite_e import hermeder

series = np.array([1, 2, 3, 4, 5, 10])

# using np.harmeder() method
gfg = hermeder(series, m = 3)

print(gfg)
```

**输出:**

> [24\. 120\. 600.]