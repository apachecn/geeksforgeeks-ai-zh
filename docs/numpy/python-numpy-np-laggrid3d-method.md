# Python | Numpy NP . lagrid3d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lagrid 3d-method/](https://www.geeksforgeeks.org/python-numpy-np-laggrid3d-method/)

`**np.laggrid3d()**`方法用于计算 x，y 和 z 的笛卡尔乘积上的三维拉盖尔级数。

> **语法:** `np.laggrid3d(x, y, z, c)`
> **参数:**
> **x，y，z:**【array _ like】三维数列在 x，y，z 的笛卡儿积中的点处求值。如果 x 或 y 或 z 是列表或元组，则首先将其转换为数组，否则保持不变，如果不是数组，则将其视为标量。
> **c:**【array _ like】从低到高排序的拉盖尔级数系数的一维数组。
> 
> **返回:**【ndarray】二维切比雪夫级数在 x 和 y 的笛卡尔乘积中的点上的值

**代码#1 :**

```
# Python program explaining
# numpy.laggrid3d() method 

# importing numpy as np

import numpy as np 
from numpy.polynomial.laguerre import laggrid3d

# Input laguerre series coefficients
c = np.array([[1, 3, 5], [2, 4, 6], [10, 11, 12]]) 

# using np.laggrid3d() method 
ans = laggrid3d([7, 9], [8, 10], [5, 6], c)
print(ans)
```

**Output:**

```
[[ -9521.5 -12198\. ]
 [-19782.5 -25346\. ]]

```

**代码#2 :**

```
# Python program explaining
# numpy.laggrid3d() method 

# importing numpy as np 
import numpy as np 
from numpy.polynomial.laguerre import laggrid3d

# Input laguerre series coefficients
c = np.array([[1, 3, 5], [2, 4, 6], [10, 11, 12]]) 

# using np.laggrid3d() method 
ans = laggrid3d(7, 11, 12, c)

print(ans)
```

**Output:**

```
3275.5

```