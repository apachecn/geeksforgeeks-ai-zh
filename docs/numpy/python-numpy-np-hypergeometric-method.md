# Python | Numpy np .超几何()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-超几何-方法/](https://www.geeksforgeeks.org/python-numpy-np-hypergeometric-method/)

借助`**np.hypergeometric()**`方法，利用`np.hypergeometric()`方法可以得到阵列形式的超几何分布。

> **语法:** `np.hypergeometric(ngood, nbad, samples, size)`
> **返回:**返回超几何分布的数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.hypergeometric()`方法，我们能够以数组的形式获得超几何分布。

```py
# import numpy
import numpy as np

# using np.hypergeometric() method
gfg = np.random.hypergeometric(50, 5, 5, 20)

print(gfg)
```

**输出:**

> 数组([4，5，5，5，4，5，5，5，4，5，4，4，5，4，5，5，3，5，4，5，5])

**例 2 :**

```py
# import numpy
import numpy as np

# using np.hypergeometric() method
gfg = np.random.hypergeometric(150, 50, 50, 20)

print(gfg)
```

**输出:**

> [37 35 40 33 43 37 38 38 36 41 42 32 36 35 36 38 35 35 36 35]