# Python | Numpy np.disp()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-np-disp-method/](https://www.geeksforgeeks.org/python-numpy-np-disp-method/)

借助`**np.disp()**`方法，我们可以将字符串放入显示缓冲区，通过使用 stringIO 类，我们可以使用`np.disp()`方法从缓冲区中获取值。

> **语法:** `np.disp(message, device)`
> **返回:**没有 StringIO 类不会返回任何东西。

**示例#1 :**
在本例中，通过使用`np.disp()`方法，我们能够从参数中收集消息，并使用该方法将该消息放入显示缓冲区。

```
# import numpy and stringIO
import numpy as np
from io import StringIO

buf = StringIO()
# using np.disp() method
np.disp(u'Geeks For Geeks', device = buf)
buf.getvalue()
```

**输出:**

> 极客的极客\n '

**例 2 :**

```
# import numpy and stringIO
import numpy as np
from io import StringIO

buf = StringIO()
# using np.disp() method
np.disp(u'Author "Jitender Kumar"', device = buf)
buf.getvalue()
```

**输出:**

> 作者“吉坦德·库马尔”