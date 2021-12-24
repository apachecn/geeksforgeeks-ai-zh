# Python | Numpy NP . hermone()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-NP-hermone-method/](https://www.geeksforgeeks.org/python-numpy-np-hermeone-method/)

借助`**np.hermeone()**`法，我们可以用**赫曼**代替`np.ones()`用`np.hermeone()`法。

> **语法:** `np.hermeone`
> **返回:**返回一气呵成的阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hermeone()`方法，我们能够获得与该方法相同的`np.ones`功能。

```
# import numpy and hermeone
import numpy as np
from numpy.polynomial.hermite_e import hermeone

# using np.hermeone() method
gfg = hermeone + [1, 2, 3, 4, 5]

print(gfg)
```

**输出:**

> [2 3 4 5 6]

**例 2 :**

```
# import numpy and hermeone
import numpy as np
from numpy.polynomial.hermite_e import hermeone

# using np.hermeone() method
gfg = hermeone + [[2, 4, 6], [3, 6, 9]]

print(gfg)
```

**输出:**

> [[3 5 7]
> [4 7 10]]