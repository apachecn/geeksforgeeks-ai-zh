# Python | Numpy np .多项式()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-多项式-method/](https://www.geeksforgeeks.org/python-numpy-np-multinomial-method/)

借助`**np.multinomial()**`方法，利用`np.multinomial()`方法可以得到多项式分布的数组。

> **语法:** `np.multinomial(n, nval, size)`
> **返回:**返回多项式分布的数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.multinomial()`方法，我们能够使用该方法获得多项式分布数组。

```
# import numpy
import numpy as np

# using np.multinomial() method
gfg = np.random.multinomial(8, [0.1, 0.22, 0.333, 0.4444], 2)

print(gfg)
```

**输出:**

> [[1 4 2 1]
> [0 0 3 5]]

**例 2 :**

```
# import numpy
import numpy as np

# using np.multinomial() method
gfg = np.random.multinomial(12, [0.1, 0.12, 0.123, 0.1234, 0.12345], 3)

print(gfg)
```

**输出:**

> [[2 0 1 1 8]
> [0 1 1 9]
> [1 1 0 9]]