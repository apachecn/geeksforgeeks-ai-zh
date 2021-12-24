# Python | Numpy np.chebpow()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-cheb pow-method/](https://www.geeksforgeeks.org/python-numpy-np-chebpow-method/)

借助`**np.chebpow()**`法，利用`np.chebpow()`法可以得到**切比雪夫系列**的功率。

> **语法:** `np.chebpow(s1, power)`
> **返回:**幂级数后返回一个数组。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.chebpow()`方法，我们能够使用这个方法得到切比雪夫级数的幂。

```py
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (4, 6, 8)

# using np.chebpow() method
gfg = C.chebpow(s1, 5)

print(gfg)
```

**输出:**

> [224664.429180.381240.305790.227400.151206.91560.47040.21760.
> 7680。2048.]

**例 2 :**

```py
# import numpy
import numpy as np
from numpy.polynomial import chebyshev as C

s1 = (3, 5, 7, 2, 4, 6)

# using np.chebpow() method
gfg = C.chebpow(s1, 2)

print(gfg)
```

**输出:**

> [ 74\. 111\. 104.5 109\. 88.5 70\. 60\. 50\. 20\. 24\. 18\. ]