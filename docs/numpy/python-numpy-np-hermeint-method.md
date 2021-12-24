# python | num py NP . hermint()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-hermaint-method/](https://www.geeksforgeeks.org/python-numpy-np-hermeint-method/)

借助`**np.hermeint()**`方法，我们可以用`np.hermeint()`方法积分 hermiteE 级数。

> **语法:** `np.hermeint(series, m)`
> 
> **返回:**返回积分级数的系数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermeint()`方法，我们能够用这个方法得到 hermiteE 级数的积分级数系数。

```
# import numpy and harmeint
import numpy as np
from numpy.polynomial.hermite_e import hermeint

series = np.array([2, 0.3, 4, 0.5, 6])

# using np.harmeint() method
gfg = hermeint(series, m = 2)

print(gfg)
```

**输出:**

> [3\. -0.225 1\. 0.05 0.33333333 0.025 0.2]

**例 2 :**

```
# import numpy and harmeint
import numpy as np
from numpy.polynomial.hermite_e import hermeint

series = np.array([1, 2, 3, 4, 5])

# using np.harmeint() method
gfg = hermeint(series, m = 3)

print(gfg)
```

**输出:**

> [-0.75 2.25 -1\. 0.16666667 0.08333333 0.05 0.03333333 0.02380952]