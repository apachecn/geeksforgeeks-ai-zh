# Python | Numpy np.logseries()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-log series-method/](https://www.geeksforgeeks.org/python-numpy-np-logseries-method/)

借助`**np.logseries()**`方法，利用`np.logseries()`方法可以得到数组形式的对数级数。

> **语法:** `np.logseries(p, size)`
> 
> **返回:**返回一组日志序列。

**示例#1 :**

在这个例子中我们可以看到，通过使用`np.logseries()`方法，我们能够通过使用这个方法得到一个对数序列的数组。

```
# import numpy
import numpy as np

# using np.logseries() method
gfg = np.random.logseries(0.4, 25)

print(gfg)
```

**输出:**

> [1 1 1 3 1 2 1 1 2 1 1 1 1 1 1 1 1 1 2 3 1 3 1 1 1]

**例 2 :**

```
# import numpy
import numpy as np

# using np.logseries() method
gfg = np.random.logseries(0.8, 25)

print(gfg)
```

**输出:**

> 1 1 1 2 3 1 6 3 3 3 1 2 1 1 1 5 2 1 18 1 1 1 2