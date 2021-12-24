# Python | Numpy NP . lagrid2d()方法

> 原文:[https://www . geeksforgeeks . org/python-numpy-NP-lagrid2d-method/](https://www.geeksforgeeks.org/python-numpy-np-laggrid2d-method/)

`**np.laggrid2d()**`方法用于计算 x 和 y 的笛卡尔乘积上的二维拉盖尔级数。

> **语法:** `np.laggrid2d(x, y, c)`
> **参数:**
> **x，y:**【array _ like】二维数列在 x 和 y 的笛卡尔乘积中的点处求值。如果 x 或 y 是列表或元组，则首先将其转换为 ndarray，否则保持不变，如果不是 ndarray，则将其视为标量。
> **c:**【array _ like】从低到高排序的拉盖尔级数系数的一维数组。
> 
> **返回:**【ndarray】二维切比雪夫级数在 x 和 y 的笛卡尔乘积中的点上的值

**代码#1 :**

```
# Python program explaining
# numpy.laggrid2d() method 

# importing numpy as np

import numpy as np 
from numpy.polynomial.laguerre import laggrid2d

# Input laguerre series coefficients
c = np.array([[1, 3, 5], [2, 4, 6]]) 

# using np.laggrid2d() method 
ans = laggrid2d([7, 9], [8, 10], c)
print(ans)
```

**Output:**

```
[[ -391\.  -783.]
 [ -543\. -1087.]]

```

**代码#2 :**

```
# Python program explaining
# numpy.laggrid2d() method 

# importing numpy as np 
import numpy as np 
from numpy.polynomial.laguerre import laggrid2d

# Input laguerre series coefficients
c = np.array([[1, 3, 5], [2, 4, 6]]) 

# using np.laggrid2d() method 
ans = laggrid2d(7, 8, c)

print(ans)
```

**Output:**

```
-391.0

```