# Python | Numpy np.lagone()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-NP-lagone 方法/

可以使用`**np.lagone()**`方法代替**NP . one**来创建元素为 1 的数组。

> **语法:** `np.lagone()`
> **返回:**返回数组([1])

**示例#1 :**

```py

# Python program explaining
# numpy.lagone() method 

# import numpy and lagone
import numpy as np
from numpy.polynomial.laguerre import lagone

# using np.lagone() method
ans = lagone

print(ans)
```

**输出:**

> [1]

**例 2 :**

```py
# Python program explaining
# numpy.lagone() method 

# import numpy and lagone
import numpy as np
from numpy.polynomial.laguerre  import lagone

# using np.lagone() method
ans = lagone + [[1, 3, 5], [2, 4, 6]]

print(ans)
```

**输出:**

> [[2 4 6]
> [3 5 7]]