# Python | Numpy np.unique()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-unique-method/](https://www.geeksforgeeks.org/python-numpy-np-unique-method/)

借助`**np.unique()**`方法，我们可以从一个在`np.unique()`方法中作为参数给出的数组中得到唯一的值。

> **语法:** `np.unique(Array)`
> **返回:**返回一个阵的唯一。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.unique()`方法，我们能够使用该方法从数组中获取唯一值。

```
# import numpy
import numpy as np

a = [1, 2, 2, 4, 3, 6, 4, 8]

# using np.unique() method
gfg = np.unique(a)

print(gfg)
```

**输出:**

> [1 2 3 4 6 8]

**例 2 :**

```
# import numpy
import numpy as np

a = [[10.2, 21.4, 3.6, 14.8], [1.0, 5.0, 10.0, 15.0]]

# using np.unique() method
gfg = np.unique(a)

print(gfg)
```

**输出:**

> [1\. 3.6 5\. 10\. 10.2 14.8 15\. 21.4]