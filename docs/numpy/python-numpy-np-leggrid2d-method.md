# Python | Numpy np.leggrid2d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-leggrid2d-method/](https://www.geeksforgeeks.org/python-numpy-np-leggrid2d-method/)

`**np.leggrid2d()**`方法用于计算 x 和 y 的笛卡尔乘积上的二维勒让德级数。

> **语法:** `np.leggrid2d(x, y, c)`
> **参数:**
> **x，y:**【array _ like】二维数列在 x 和 y 的笛卡尔乘积中的点处求值。如果 x 或 y 是列表或元组，则首先将其转换为 ndarray，否则保持不变，如果不是 ndarray，则将其视为标量。
> **c:**【array _ like】勒让德级数系数从低到高排序的一维数组。
> 
> **返回:**【ndarray】二维勒让德级数在 x 和 y 的笛卡尔乘积中的点上的值。

**代码#1 :**

```py
# Python program explaining
# numpy.leggrid2d() method 

# importing numpy as np

import numpy as np 
from numpy.polynomial.legendre import leggrid2d

# Input legendre series coefficients
c = np.array([[1, 3, 5], [2, 4, 6]]) 

# using np.leggrid2d() method 
ans = leggrid2d([7, 9], [8, 10], c)
print(ans)
```

**Output:**

```py
[[ 4751.5  7351.5]
 [ 5965.5  9229.5]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.leggrid2d() method 

# importing numpy as np 
import numpy as np 
from numpy.polynomial.legendre import leggrid2d

# Input legendre series coefficients
c = np.array([[1, 3, 5], [2, 4, 6]]) 

# using np.leggrid2d() method 
ans = leggrid2d(7, 8, c)

print(ans)
```

**Output:**

```py
4751.5

```