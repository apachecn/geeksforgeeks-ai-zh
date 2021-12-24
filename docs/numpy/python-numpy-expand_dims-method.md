# Python | Numpy.expand_dims()方法

> 原文:[https://www . geesforgeks . org/python-numpy-expand _ dims-method/](https://www.geeksforgeeks.org/python-numpy-expand_dims-method/)

借助`**Numpy.expand_dims()**`方法，我们可以用`Numpy.expand_dims()`方法得到一个数组的展开维数。

> **语法:** `Numpy.expand_dims()`
> 
> **返回:**返回展开的数组。

**示例#1 :**
在这个示例中，我们可以看到，使用`Numpy.expand_dims()`方法，我们能够使用该方法获得扩展数组。

```py
# import numpy
import numpy as np

# using Numpy.expand_dims() method
gfg = np.array([1, 2])
print(gfg.shape)

gfg = np.expand_dims(gfg, axis = 0)
print(gfg.shape)
```

**输出:**

> (2)、
> (1、2)

**例 2 :**

```py
# import numpy
import numpy as np

# using Numpy.expand_dims() method
gfg = np.array([[1, 2], [7, 8]])
print(gfg.shape)

gfg = np.expand_dims(gfg, axis = 0)
print(gfg.shape)
```

**输出:**

> (2，2)
> (1，2，2)