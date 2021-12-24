# Python | Numpy np.lagzero()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag zero-method/](https://www.geeksforgeeks.org/python-numpy-np-lagzero-method/)

可以使用`**np.lagzero()**`方法代替**NP . zeross**来创建元素为 0 的数组。

> **语法:** `np.lagzero()`
> **返回:**返回数组([0])

**示例#1 :**

```

# Python program explaining
# numpy.lagzero() method 

# import numpy and lagzero
import numpy as np
from numpy.polynomial.laguerre import lagzero

# using np.lagzero() method
ans = lagzero

print(ans)
```

**输出:**

> [0]

**例 2 :**

```
# Python program explaining
# numpy.lagzero() method 

# import numpy and lagzero
import numpy as np
from numpy.polynomial.laguerre  import lagzero

# using np.lagzero() method
ans = lagzero + [[1, 3, 5], [2, 4, 6]]

print(ans)
```

**输出:**

> [[1 3 5]
> [2 4 6]]