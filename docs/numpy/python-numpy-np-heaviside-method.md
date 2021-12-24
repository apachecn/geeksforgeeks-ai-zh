# Python | Numpy np.heaviside()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-heaviside-method/](https://www.geeksforgeeks.org/python-numpy-np-heaviside-method/)

借助`**np.heaviside()**`方法，我们可以用`np.heaviside()`方法得到阶梯函数。
T3】

> **句法:** `np.heaviside(array1, array2 or value)`
> **回位:**回位天问系列。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.heaviside()`方法，我们能够通过使用这个方法来获得一系列重指数阶跃函数的数组。

```
# import numpy
import numpy as np

x = np.array([-1.5, 0.5, 0, 0.5, 1.5])
# using np.heaviside() method
gfg = np.heaviside(x, 0.5)

print(gfg)
```

**输出:**

> [0\. 1\. 0.5 1\. 1.]

**例 2 :**

```
# import numpy
import numpy as np

x = np.zeros(5)
y = np.array([-1.5, 0.5, 0, 0.5, -1.5])

# using np.heaviside() method
gfg = np.heaviside(x, y)

print(gfg)
```

**输出:**

> [-1.5 0.5 0\. 0.5 -1.5]