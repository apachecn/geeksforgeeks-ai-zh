# Python | Numpy np.mask_or()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-mask _ or-method/](https://www.geeksforgeeks.org/python-numpy-np-mask_or-method/)

借助`**np.mask_or()**`方法，我们可以使用`np.mask_or()`方法将两个掩码与逻辑**或**运算符结合起来。

> **语法:** `np.mask_or(m1, m2)`
> **返回:**用逻辑或运算符返回掩码。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.mask_or()`方法，我们能够使用该方法获得带有逻辑 OR 运算符的两个掩码。

```py
# import numpy and mask_or
import numpy as np

m1 = np.array([1, 1, 0, 1])
m2 = np.array([0, 0, 1, 1])

# using np.mask_or() method
gfg = np.ma.mask_or(m1, m2)

print(gfg)
```

**输出:**

> [真真真真]

**例 2 :**

```py
# import numpy and mask_or
import numpy as np

m1 = np.array([1, 0, 0, 1, 0])
m2 = np.array([0, 0, 1, 1, 0])

# using np.mask_or() method
gfg = np.ma.mask_or(m1, m2)

print(gfg)
```

**输出:**

> [真真假假真真假假]