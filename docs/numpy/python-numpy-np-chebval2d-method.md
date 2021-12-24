# python | num py NP . chebv 2d()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-NP-chebv 2d-method/

借助`**np.chebval2d()**`方法，利用`np.chebval2d()`方法可以得到切比雪夫级数上(x，y)求值后的系数数组。

> **语法:** `np.chebval2d(x, y, c)`
> **返回:**在(x，y)上求值后返回数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.chebval2d()`方法，我们能够通过评估切比雪夫级数上的(x，y)来获得系数数组。

```
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebval2d() method
gfg = cheb.chebval2d((2, 5), (1, 3), (2, -4, 1))

print(gfg)
```

**输出:**

> [32\. 94.]

**例 2 :**

```
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebval2d() method
gfg = cheb.chebval2d((1, 3, 5, 7), (2, 4, 8), (2, -4, 1, 5, 1))

print(gfg)
```

**输出:**

> [719680\. 6486180\. 52831708.]