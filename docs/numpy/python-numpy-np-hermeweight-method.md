# Python | Numpy np.hermeweight()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermeweight-method/](https://www.geeksforgeeks.org/python-numpy-np-hermeweight-method/)

借助`**np.hermeweight()**`方法，利用`np.hermeweight()`方法可以得到 hermiteE 多项式的权函数。

> **语法:** `np.hermeweight(polynomial)`
> **返回:**返回 hermiteE 多项式的权函数。

**示例#1 :**
在这个示例中我们可以看到，通过使用`np.hermeweight()`方法，我们能够使用该方法获得 hermiteE 多项式的权函数。

```
# import numpy and hermeweight
import numpy as np
from numpy.polynomial.hermite_e import hermeweight

poly = np.array([0.1, 0.2, 0.3])

# using np.hermeweight() method
gfg = hermeweight(poly)

print(gfg)
```

**输出:**

> [0.99501248 0.98019867 0.95599748]

**例 2 :**

```
# import numpy and hermeweight
import numpy as np
from numpy.polynomial.hermite_e import hermeweight

poly = np.array([1.1, 2.2, 3.3, 4.4])

# using np.hermeweight() method
gfg = hermeweight(poly)

print(gfg)
```

**输出:**

> [5.46074427 e-01 8.89216175 e-02 4.31784001 e-03 6.25215038 e-05]