# python \ numpy 例如 lagrantrim()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag trim-method/](https://www.geeksforgeeks.org/python-numpy-np-lagtrim-method/)

借助`**np.lagtrim()**`方法，我们可以使用`np.lagtrim()`方法修剪多项式的小拖尾值。

> **语法:** `np.lagtrim(c, tol)`
> **返回:**返回多项式的修剪值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.lagtrim()`方法，我们能够通过使用该方法移除尾随值来获得多项式的修剪值。

```
# import numpy and lagtrim
import numpy as np
from numpy.polynomial.laguerre import lagtrim

# using np.lagtrim() method
gfg = lagtrim([1, 2, 3, 0, 0], 0)

print(gfg)
```

**输出:**

> [1\. 2\. 3.]

**例 2 :**

```
# import numpy and lagtrim
import numpy as np
from numpy.polynomial.laguerre import lagtrim

# using np.lagtrim() method
gfg = lagtrim([0, 1, 2, 3], 3)

print(gfg)
```

**输出:**

> [0.]