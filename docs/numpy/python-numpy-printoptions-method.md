# Python | numpy.printoptions()方法

> 原文:[https://www . geesforgeks . org/python-numpy-print options-method/](https://www.geeksforgeeks.org/python-numpy-printoptions-method/)

借助`**numpy.printoptions()**`方法，我们可以获得自定义打印选项，就像我们可以使用`numpy.printoptions()`方法设置浮点值的精度一样。

> **语法:** `numpy.printoptions(precision=value)`
> **返回:**返回定制打印喜欢的精度。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`numpy.printoptions()`方法，我们可以获得定制的打印选项，就像我们可以设置精度值一样。

```
# import numpy
import numpy as np

# using numpy.printoptions() method
with np.printoptions(precision = 3):
     print(np.array([1, 2, 3])/2.38)
```

**输出:**

> [0.42 0.84 1.261]

**例 2 :**

```
# import numpy
import numpy as np

# using numpy.printoptions() method
with np.printoptions(precision = 5):
     print(np.array([[5, 10, 15], [20, 25, 30], [35, 40, 45]])/2.3865)
```

**输出:**

> 【【2.09512 4.19024 6.28536】
> 【8.38047 10.47559 12.57071】
> 【14.66583 16.76095 18.85607】】