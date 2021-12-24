# Python | numpy.isnat()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-isnat-method/](https://www.geeksforgeeks.org/python-numpy-isnat-method/)

借助`**numpy.isnat()**`方法，如果在一个`np.datetime64()`方法中定义的日期不是时间，我们可以通过使用`numpy.isnat()`方法得到布尔值为真。

> **语法:** `numpy.isnat()`
> **返回:**如果找不到时间返回布尔值。

**例#1 :**
在这个例子中我们可以看到，通过使用`numpy.isnat()`方法，如果在`np.datetime64()`方法中没有找到时间，我们就能够得到布尔值。

```
# import numpy
import numpy as np

# using numpy.isnat() method
gfg = np.isnat(np.datetime64("Nat"))

print(gfg)
```

**输出:**

> 真实的

**例 2 :**

```
# import numpy
import numpy as np

# using numpy.isnat() method
gfg = np.isnat(np.datetime64("1998-01-01"))

print(gfg)
```

**输出:**

> 错误的