# Python | Numpy expandtabs()方法

> 原文:[https://www . geesforgeks . org/python-numpy-expandtabs-method/](https://www.geeksforgeeks.org/python-numpy-expandtabs-method/)

借助`**numpy.char.expandtabs()**`方法，我们可以在单条语句中使用 numpy 方法展开选项卡。

> **语法:** `numpy.char.expandtabs()`
> 
> **返回:**返回已展开制表符的字符串数组。

**示例#1 :**

在这个例子中，我们可以看到，通过使用`numpy.char.expandtabs()`方法，我们能够通过使用 numpy 获得扩展的选项卡。

```
# import numpy
import numpy as np

# using numpy.char.expandtabs() method
gfg = np.char.expandtabs(['Geeks\tFor\tGeeks'], 10)

print(gfg)
```

**输出:**

> [“极客为极客”]

**例 2 :**

```
# import numpy
import numpy as np

# using numpy.char.expandtabs() method
gfg = np.char.expandtabs(['G\tF\tG', 'Jitender\tKumar'], 20)

print(gfg)
```

**输出:**

> [' g g ' jitter Kumar ']