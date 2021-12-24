# Python | Numpy np.polygrid2d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-polygrid 2d-method/](https://www.geeksforgeeks.org/python-numpy-np-polygrid2d-method/)

`**np.polygrid2d()**`方法用于计算 x 和 y 的笛卡尔乘积上的二维多项式级数。

> **语法:** `np.polygrid2d(x, y, c)`
> **参数:**
> **x，y:**【array _ like】二维数列在 x 和 y 的笛卡尔乘积中的点处求值。如果 x 或 y 是列表或元组，则首先将其转换为 ndarray，否则保持不变，如果不是 ndarray，则将其视为标量。
> **c:**【array _ like】系数多项式级数的数组。
> **Return:**【ndarray】二维多项式级数在 x 和 y 的笛卡尔乘积中的点处的值。

**代码#1 :**

```py
# Python program explaining
# numpy.polygrid2d() method 

# importing numpy as np

import numpy as np 
from numpy.polynomial.polynomial import polygrid2d

# Input polynomial series coefficients
c = np.array([[1, 3, 5], [2, 4, 6]]) 

# using np.polygrid2d() method 
ans = polygrid2d([7, 9], [8, 10], c)
print(ans)
```

**Output:**

```py
[[ 3271\.  5025.]
 [ 4107\.  6309.]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.polygrid2d() method 

# importing numpy as np 
import numpy as np 
from numpy.polynomial.polynomial import polygrid2d

# Input polynomial series coefficients
c = np.array([[1, 3, 5], [2, 4, 6]]) 

# using np.polygrid2d() method 
ans = polygrid2d(7, 8, c)

print(ans)
```

**Output:**

```py
3271.0

```