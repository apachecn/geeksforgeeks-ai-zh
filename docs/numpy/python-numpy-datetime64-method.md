# Python | numpy.datetime64()方法

> 原文:[https://www . geesforgeks . org/python-numpy-datetime 64-method/](https://www.geeksforgeeks.org/python-numpy-datetime64-method/)

借助`**numpy.datetime64()**`方法，我们可以用`numpy.datetime64()`方法得到特定格式的 numpy 数组中的日期，即年-月-日。

> **语法:** `numpy.datetime64(date)`
> **返回:**以‘yyyy-mm-DD’格式返回日期。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`numpy.datetime64()`方法，我们能够获得特定格式的日期，即 yyyy-mm-dd。

```py
# import numpy
import numpy as np

# using numpy.datetime64() method
gfg = np.array(np.datetime64('2019-08-26'))

print(gfg)
```

**输出:**

> 数组(' 2019-08-26 '，dttype = ' datetime 64[d])

**例 2 :**

```py
# import numpy
import numpy as np

# using numpy.datetime64() method
gfg = np.array(np.datetime64('2019-08', 'D'))

print(gfg)
```

**输出:**

> 数组(' 2019-08-01 '，dttype = ' datetime 64[d])