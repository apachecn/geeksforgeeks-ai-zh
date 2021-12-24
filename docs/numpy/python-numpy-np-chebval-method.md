# python | num py NP . chebv()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-chebval-method/](https://www.geeksforgeeks.org/python-numpy-np-chebval-method/)

借助`**np.chebval()**`方法，利用`np.chebval()`方法可以得到切比雪夫级数上的 x 求值后的系数数组。

> **语法:** `np.chebval(x, c)`
> **返回:**在 x 上求值后返回数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.chebval()`方法，我们能够通过评估切比雪夫级数上的 x 来获得系数数组。

```
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebval() method
gfg = cheb.chebval((2, 5), (2, -4, 1))

print(gfg)
```

**输出:**

> [ 1\. 31.]

**例 2 :**

```
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebval() method
gfg = cheb.chebval((1, 3, 5, 7), (2, -4, 1, 5, 1))

print(gfg)
```

**输出:**

> [5.0000 e+00 1.0790 e+03 7.2570 e+03 2.5643 e+04]