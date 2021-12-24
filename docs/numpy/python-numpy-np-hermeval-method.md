# Python | Numpy np.hermeval()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-herm eval-method/](https://www.geeksforgeeks.org/python-numpy-np-hermeval-method/)

借助`**np.hermeval()**`方法，我们可以求 x 上的 hermite 级数，其中 s 是在`np.hermeval()`方法中定义的。

> **语法:** `np.hermeval(x, series)`
> **返回:**返回被评估的隐士系列。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermeval()`方法，我们能够用这个方法来计算 x 上的 hermite 级数。

```py
# import numpy and hermeval
import numpy as np
from numpy.polynomial.hermite import hermeval

series = np.array([1, 2, 3, 4])

# using np.hermeval() method
gfg = hermeval(2, series)

print(gfg)
```

**输出:**

> Twenty-two

**例 2 :**

```py
# import numpy and hermeval
import numpy as np
from numpy.polynomial.hermite_e import hermeval

series = np.array([1, 2, 3, 4])

# using np.hermeval() method
gfg = hermeval([[2, 3], [5, 6]], series)

print(gfg)
```

**输出:**

> [[ 22.103.】
> 【523。910.]]