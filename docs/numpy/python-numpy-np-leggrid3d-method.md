# Python | Numpy np.leggrid3d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-leggrid 3d-method/](https://www.geeksforgeeks.org/python-numpy-np-leggrid3d-method/)

`**np.leggrid3d()**`方法用于计算 x，y 和 z 的笛卡尔乘积上的三维勒让德级数。

> **语法:** `np.leggrid3d(x, y, z, c)`
> **参数:**
> **x，y，z:**【array _ like】三维数列在 x，y，z 的笛卡儿积中的点处求值。如果 x 或 y 或 z 是列表或元组，则首先将其转换为数组，否则保持不变，如果不是数组，则将其视为标量。
> **c:**【array _ like】勒让德级数系数。
> 
> **返回:**【ndarray】二维勒让德级数在 x 和 y 的笛卡尔乘积中的点上的值。

**代码#1 :**

```py
# Python program explaining
# numpy.leggrid3d() method 

# importing numpy as np

import numpy as np 
from numpy.polynomial.legendre import leggrid3d

# Input legendre series coefficients
c = np.array([[1, 3, 5], [2, 4, 6], [10, 11, 12]]) 

# using np.leggrid3d() method 
ans = leggrid3d([7, 9], [8, 10], [5, 6], c)
print(ans)
```

**Output:**

```py
[[  878011\.   1034500.5]
 [ 1351191\.   1592014.5]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.leggrid3d() method 

# importing numpy as np 
import numpy as np 
from numpy.polynomial.legendre import leggrid3d

# Input legendre series coefficients
c = np.array([[1, 3, 5], [2, 4, 6], [10, 11, 12]]) 

# using np.leggrid3d() method 
ans = leggrid3d(7, 11, 12, c)

print(ans)
```

**Output:**

```py
176982.0

```