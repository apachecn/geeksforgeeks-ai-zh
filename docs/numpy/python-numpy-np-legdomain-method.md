# Python | Numpy np.legdomain()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-leg domain-method/](https://www.geeksforgeeks.org/python-numpy-np-legdomain-method/)

借助`**np.legdomain()**`方法，我们可以得到勒让德级数中具有值**数组([-1，1])** 的滤波器。

> **语法:** `np.legdomain`
> **返回:**返回数组的过滤器([-1，1])

**示例#1 :**

```
# Python program explaining
# numpy.legdomain() method 

# import numpy and legdomain
import numpy as np
from numpy.polynomial.legendre import legdomain

# using np.legdomain() method
for i in range(5):
    ans = legdomain + [i, i + 1]
    print(ans)
```

**输出:**

> [-1 2]
> 【0 3】
> 【1 4】
> 【2 5】
> 【3 6】

**例 2 :**

```
# Python program explaining
# numpy.legdomain() method 

# import numpy and legdomain
import numpy as np
from numpy.polynomial.legendre import legdomain

# using np.legdomain() method
for i in range(4):
    ans = legdomain + [i-1, i + 1]
    print(ans)
```

**输出:**

> [-2 2]
> [-1 3]
> [0 4]
> [1 5]