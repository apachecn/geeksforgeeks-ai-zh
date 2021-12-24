# Python | Numpy np.can_cast()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-can _ cast-method/](https://www.geeksforgeeks.org/python-numpy-np-can_cast-method/)

借助`**np.can_cast()**`方法，我们可以得到一个完美的想法:使用`np.can_cast()`方法，一个数据类型是否可以转换成另一个数据类型。

> **语法:** `np.can_cast(source data_type, target data_type)`
> **返回:**当可以做其他事情时，将布尔值返回为真，否则返回假。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.can_cast()`方法，当使用该方法可以执行强制转换时，我们可以将布尔值设置为真，否则为假。

```
# import numpy
import numpy as np

# using np.can_cast() method
gfg = np.can_cast(np.int32, np.int64)

print(gfg)
```

**输出:**

> 真实的

**例 2 :**

```
# import numpy
import numpy as np

# using np.can_cast() method
gfg = np.can_cast(5.5e10, np.int32)

print(gfg)
```

**输出:**

> 错误的