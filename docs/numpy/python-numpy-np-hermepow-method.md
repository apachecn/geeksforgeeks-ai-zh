# python | num py NP . herm pow()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-NP-herm pow 方法/

借助`**np.hermepow()**`方法，我们可以用`np.hermepow()`方法得到 hermiteE 级数的一次幂。

> **语法:** `np.hermepow(series, power)`
> **回归:**回归动力 hermiteE 系列。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermepow()`方法，我们能够通过使用这个方法得到 hermiteE 级数的幂的提升。

```
# import numpy and hermepow
import numpy as np
from numpy.polynomial.hermite_e import hermepow

series = np.array([1, 2, 3, 4])

# using np.hermepow() method
gfg = hermepow(series, 2)

print(gfg)
```

**输出:**

> [119\. 172\. 382\. 164\. 169\. 24\. 16.]

**例 2 :**

```
# import numpy and hermepow
import numpy as np
from numpy.polynomial.hermite_e import hermepow

series = np.array([11, 22, 33, 44])

# using np.hermepow() method
gfg = hermepow(series, 3)

print(gfg)
```

**输出:**

> [8905721.41678934.43080477.65016688.26261961.
> 22847946。4316433.2571492.191664.85184.]