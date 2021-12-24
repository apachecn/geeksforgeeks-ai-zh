# Python | Numpy np.hermedomain()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermedomain-method/](https://www.geeksforgeeks.org/python-numpy-np-hermedomain-method/)

借助`**np.hermedomain()**`方法，利用`np.hermedomain()`方法可以得到 hermiteE 级数中具有值**数组([-1，1])** 的滤波器。

> **语法:** `np.hermedomain`
> **返回:**返回数组的过滤器([-1，1])

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermedomain()`方法，我们能够使用该方法获得 hermiteE 系列中的**数组([-1，1])** 的过滤器。

```
# import numpy and hermedomain
import numpy as np
from numpy.polynomial.hermite_e import hermedomain

# using np.hermedomain() method
for i in range(5):
    gfg = hermedomain + [i, i + 1]
    print(gfg)
```

**输出:**

> [-1 2]
> 【0 3】
> 【1 4】
> 【2 5】
> 【3 6】

**例 2 :**

```
# import numpy and hermedomain
import numpy as np
from numpy.polynomial.hermite_e import hermedomain

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