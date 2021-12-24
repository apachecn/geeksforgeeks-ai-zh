# Python | Numpy NP . chebrots()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-chebrouts-method/](https://www.geeksforgeeks.org/python-numpy-np-chebroots-method/)

借助`**np.chebroots()**`方法，利用`np.chebroots()`方法可以得到切比雪夫级数的根。

> **语法:** `np.chebroots(array of coefficients)`
> **返回:**返回切比雪夫数列的有根数组。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.chebroots()`方法，我们能够用这个方法得到切比雪夫级数的根。

```py
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebroots() method
gfg = cheb.chebroots((2, 4, 8, 1))

print(gfg)
```

**输出:**

> [-3.83265557 -0.71484143 0.54749701]

**例 2 :**

```py
# import numpy
import numpy as np
import numpy.polynomial.chebyshev as cheb

# using np.chebroots() method
gfg = cheb.chebroots((-3, 4, -5, 1, 10))

print(gfg)
```

**输出:**

> [-1.02213642 -0.38135467 0.40624906 0.94724203]