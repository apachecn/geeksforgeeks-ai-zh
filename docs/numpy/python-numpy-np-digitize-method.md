# Python | Numpy NP . digital()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-digital-method/](https://www.geeksforgeeks.org/python-numpy-np-digitize-method/)

借助于`**np.digitize()**`方法，我们可以通过`np.digitize()`方法得到每个值所属的仓的索引。

> **语法:** `np.digitize(Array, Bin, Right)`
> **返回:**返回一组仓位的指数。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.digitize()`方法，我们能够使用该方法获得属于数组的每个值的 bin 的索引数组。

```py
# import numpy
import numpy as np

a = np.array([1.2, 2.4, 3.6, 4.8])
bins = np.array([1.0, 1.3, 2.5, 4.0, 10.0])

# using np.digitize() method
gfg = np.digitize(a, bins)

print(gfg)
```

**输出:**

> [1 2 3 4]

**例 2 :**

```py
# import numpy
import numpy as np

a = np.array([[10.2, 21.4, 3.6, 14.8], [1.0, 5.0, 10.0, 15.0]])
bins = np.array([1.0, 1.3, 2.5, 4.0, 10.0])

# using np.digitize() method
gfg = np.digitize(a, bins)

print(gfg)
```

**输出:**

> [[5 5 3 5]
> [1 4 5]]