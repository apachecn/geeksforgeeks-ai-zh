# Python | Numpy np.hermegauss()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermegauss-method/](https://www.geeksforgeeks.org/python-numpy-np-hermegauss-method/)

借助`**np.hermegauss()**`方法，利用`np.hermegauss()`方法可以得到高斯 hermiteE 级数的求积。

> **语法:** `np.hermegauss(deg)`
> **返回:**返回高斯 hermiteE 级数的求积。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermegauss()`方法，我们能够利用这个方法得到高斯 hermiteE 级数的求积。

```
# import numpy as np
import numpy as np
from numpy.polynomial.hermite_e import hermegauss

# using np.hermegauss() method
gfg = hermegauss(2)

print(gfg)
```

**输出:**

> (数组([-1。, 1.])，数组([1.25331414，1.25331414])

**例 2 :**

```
# import numpy as np
import numpy as np
from numpy.polynomial.hermite_e import hermegauss

# using np.hermegauss() method
gfg = hermegauss(3)

print(gfg)
```

**输出:**

> (数组([-1.73205081，0。，1.73205081])，数组([0.41777138，1.67108552，0.41777138])