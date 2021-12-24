# Python | Numpy np.legzero()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-legzero-method/](https://www.geeksforgeeks.org/python-numpy-np-legzero-method/)

可以使用`**np.legzero()**`方法代替**NP . zeross**来创建元素为 0 的数组。

> **语法:** `np.legzero()`
> **返回:**返回数组([0])

**示例#1 :**

```py

# Python program explaining
# numpy.legzero() method 

# import numpy and legzero
import numpy as np
from numpy.polynomial.legendre import legzero

# using np.legzero() method
ans = legzero

print(ans)
```

**输出:**

> [0]

**例 2 :**

```py
# Python program explaining
# numpy.legzero() method 

# import numpy and legzero
import numpy as np
from numpy.polynomial.legendre import legzero

# using np.legzero() method
ans = legzero + [[1, 3, 5], [2, 4, 6]]

print(ans)
```

**输出:**

> [[1 3 5]
> [2 4 6]]