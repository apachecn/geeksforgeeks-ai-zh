# Python | Numpy np.polyone()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-polyone-method/](https://www.geeksforgeeks.org/python-numpy-np-polyone-method/)

可以使用`**np.polyone()**`方法代替**NP . one**来创建元素为 1 的数组。

> **语法:** `np.polyone()`
> **返回:**返回数组([1])

**示例#1 :**

```py

# Python program explaining
# numpy.polyone() method 

# import numpy and polyone
import numpy as np
from numpy.polynomial.polynomial import polyone

# using np.polyone() method
ans = polyone

print(ans)
```

**输出:**

> [1]

**例 2 :**

```py
# Python program explaining
# numpy.polyone() method 

# import numpy and polyone
import numpy as np
from numpy.polynomial.polynomial import polyone

# using np.polyone() method
ans = polyone + [[1, 3, 5], [2, 4, 6]]

print(ans)
```

**输出:**

> [[2 4 6]
> [3 5 7]]