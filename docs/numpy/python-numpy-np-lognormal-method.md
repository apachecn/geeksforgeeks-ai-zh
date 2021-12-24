# Python | Numpy np.lognormal()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-log normal-method/](https://www.geeksforgeeks.org/python-numpy-np-lognormal-method/)

借助`**np.lognormal()**`方法，我们可以用`np.lognormal()`方法得到对数正态分布值。

> **语法:** `np.lognormal(mean, sigma, size)`
> **返回:**返回对数正态分布的数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.lognormal()`方法，我们能够使用该方法获得对数正态分布。

```py
# import numpy
import numpy as np

# using np.lognormal() method
gfg = np.random.lognormal(0.4, 1, 20)

print(gfg) 
```

**输出:**

> [1.79018885 5.92534286 1.00603156 3.81479755 1.25423563 1.07349624
> 1.73633784 3.94777056 0.46396803 6.94550919 0.9945095

**例 2 :**

```py
# import numpy
import numpy as np

# using np.lognormal() method
gfg = np.random.lognormal(0.5, 3, 20)

print(gfg) 
```

**输出:**

> [3.07682048 e+00 9.44352316 e+01 6.87353998 e+03 3.05831375 e+01
> 1.46571273 e+00 3.90269093 e+01 1 1.69201799 e+01 3.85820572 e+00
> 1.06782865 e+01