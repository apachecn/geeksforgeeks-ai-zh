# Python | Numpy np.lagdomain()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag domain-method/](https://www.geeksforgeeks.org/python-numpy-np-lagdomain-method/)

借助`**np.lagdomain()**`方法，可以得到拉盖尔级数中具有值**数组(【0，1】)**的滤波器。

> **语法:** `np.lagdomain`
> **返回:**返回数组的过滤器([0，1])

**示例#1 :**

```py
# Python program explaining
# numpy.lagdomain() method 

# import numpy and lagdomain
import numpy as np
from numpy.polynomial.laguerre import lagdomain

# using np.lagdomain() method
for i in range(5):
    ans = lagdomain + [i, i + 1]
    print(ans)
```

**输出:**

> [-1 2]
> 【0 3】
> 【1 4】
> 【2 5】
> 【3 6】

**例 2 :**

```py
# Python program explaining
# numpy.lagdomain() method 

# import numpy and lagdomain
import numpy as np
from numpy.polynomial.laguerre import lagdomain

# using np.lagdomain() method
for i in range(4):
    ans = lagdomain + [i-1, i + 1]
    print(ans)
```

**输出:**

> 【-2 2】
> 【-1 3】
> 【0 4】
> 【1 5】
> 【2 6】