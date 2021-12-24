# python | num py NP . char . endcon()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-char-end swith-method/](https://www.geeksforgeeks.org/python-numpy-np-char-endswith-method/)

借助`**np.char.endswith()**`方法，当值以`np.char.endswith()`方法传递的特定字符结束时，我们可以得到布尔数组。

> **语法:** `np.char.endswith()`
> **返回:**当值以值结束时返回布尔数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.char.endswith()`方法，我们能够在与`np.char.endswith()`方法中的字符串值匹配时获得布尔数组。

```
# import numpy
import numpy as np

# using np.char.endswith() method
a = np.array(['geeks', 'for', 'geeks'])
gfg = np.char.endswith(a, 'ks')

print(gfg)
```

**输出:**

> [真假真]

**例 2 :**

```
# import numpy
import numpy as np

# using np.char.endswith() method
a = np.array([['geeks', 'for', 'geeks'], ['jitender', 'author', 'gfg']])
gfg = np.char.endswith(a, 'r')

print(gfg)
```

**输出:**

> 【【假真假】
> 【真真假】】