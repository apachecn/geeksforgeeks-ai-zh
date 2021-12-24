# Python | Numpy np.polyzero()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-polyzero-method/](https://www.geeksforgeeks.org/python-numpy-np-polyzero-method/)

可以使用`**np.polyzero()**`方法代替**NP . zeross**来创建元素为 0 的数组。

> **语法:** `np.polyzero()`
> **返回:**返回数组([0])

**示例#1 :**

```py

# Python program explaining
# numpy.polyzero() method 

# import numpy and polyzero
import numpy as np
from numpy.polynomial.polynomial import polyzero

# using np.polyzero() method
ans = polyzero

print(ans)
```

**输出:**

> [0]

**例 2 :**

```py
# Python program explaining
# numpy.polyzero() method 

# import numpy and polyzero
import numpy as np
from numpy.polynomial.polynomial  import polyzero

# using np.polyzero() method
ans = polyzero + [[1, 3, 5], [2, 4, 6]]

print(ans)
```

**输出:**

> [[1 3 5]
> [2 4 6]]