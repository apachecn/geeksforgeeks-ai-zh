# Python | Numpy np.polydomain()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-poly domain-method/](https://www.geeksforgeeks.org/python-numpy-np-polydomain-method/)

借助`**np.polydomain()**`方法，我们可以得到多项式级数形式的具有值**数组([-1，1])** 的滤波器。

> **语法:** `np.polydomain`
> **返回:**返回数组的过滤器([-1，1])

**示例#1 :**

```
# Python program explaining
# numpy.polydomain() method 

# import numpy and polydomain
import numpy as np
from numpy.polynomial.polynomial import polydomain

# using np.polydomain() method
for i in range(5):
    ans = polydomain + [i, i + 1]
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
# numpy.polydomain() method 

# import numpy and polydomain
import numpy as np
from numpy.polynomial.polynomial import polydomain

# using np.polydomain() method
for i in range(4):
    ans = polydomain + [i-1, i + 1]
    print(ans)
```

**输出:**

> [-2 2]
> [-1 3]
> [0 4]
> [1 5]