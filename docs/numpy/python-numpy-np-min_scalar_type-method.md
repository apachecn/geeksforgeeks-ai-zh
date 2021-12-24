# Python | Numpy NP . min _ scalar _ type()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-min _ scalar _ type-method/](https://www.geeksforgeeks.org/python-numpy-np-min_scalar_type-method/)

借助`**np.min_scalar_type()**`方法，我们可以得到在`np.min_scalar_type()`方法中作为参数传递的一个值的最小标量类型。

> **语法:** `np.min_scalar_type(value)`
> **返回:**返回一个值的最小标量类型。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.min_scalar_type()`方法，我们能够使用该方法获得一个值的最小标量类型。

```
# import numpy
import numpy as np

# using np.min_scalar_type() method
gfg = np.min_scalar_type(-50)

print(gfg)
```

**Output :**

> int8

**例 2 :**

```
# import numpy
import numpy as np

# using np.min_scalar_type() method
gfg = np.min_scalar_type(55.56)

print(gfg)
```

**输出:**

> 浮动 16