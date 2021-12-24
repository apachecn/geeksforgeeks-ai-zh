# Python | Numpy np.legone()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-legone-method/](https://www.geeksforgeeks.org/python-numpy-np-legone-method/)

可以使用`**np.legone()**`方法代替**NP . one**来创建元素为 1 的数组。

> **语法:** `np.legone()`
> **返回:**返回数组([1])

**示例#1 :**

```

# Python program explaining
# numpy.legone() method 

# import numpy and legone
import numpy as np
from numpy.polynomial.legendre import legone

# using np.legone() method
ans = legone

print(ans)
```

**输出:**

> [1]

**例 2 :**

```
# Python program explaining
# numpy.legone() method 

# import numpy and legone
import numpy as np
from numpy.polynomial.legendre import legone

# using np.legone() method
ans = legone + [[1, 3, 5], [2, 4, 6]]

print(ans)
```

**输出:**

> [[2 4 6]
> [3 5 7]]