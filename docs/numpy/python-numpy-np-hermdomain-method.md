# Python | Numpy np.hermdomain()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm domain-method/](https://www.geeksforgeeks.org/python-numpy-np-hermdomain-method/)

借助`**np.hermdomain()**`方法，利用`np.hermdomain()`方法可以得到 hermite 级数中具有值**数组([-1，1])** 的滤波器。

> **语法:** `np.hermdomain`
> **返回:**返回数组的过滤器([-1，1])

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermdomain()`方法，我们能够使用该方法获得埃尔米特级数中的**数组([-1，1])** 的过滤器。

```py
# import numpy and hermdomain
import numpy as np
from numpy.polynomial.hermite import hermdomain

# using np.hermdomain() method
for i in range(5):
    gfg = hermdomain + [i, i + 1]
    print(gfg)
```

**输出:**

> [-1 2]
> 【0 3】
> 【1 4】
> 【2 5】
> 【3 6】

**例 2 :**

```py
# import numpy and hermdomain
import numpy as np
from numpy.polynomial.hermite import hermdomain

# using np.hermedomain() method
for i in range(5):
    gfg = hermedomain + [i-1, i + 1]
    print(gfg)
```

**输出:**

> 【-2 2】
> 【-1 3】
> 【0 4】
> 【1 5】
> 【2 6】