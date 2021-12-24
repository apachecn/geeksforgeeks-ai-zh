# Python | Scipy integrate.simps()方法

> 原文:[https://www . geesforgeks . org/python-scipy-integrate-simps-method/](https://www.geeksforgeeks.org/python-scipy-integrate-simps-method/)

借助于`**scipy.integrate.simps()**`方法，我们可以利用沿轴的样本和复合辛普森法则通过`scipy.integrate.simps()`方法得到 y(x)的积分。

> **语法:** `scipy.integrate.simps(y, x)`
> **返回:**使用样本返回 y(x)的积分值。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`scipy.integrate.simps()`方法，我们能够使用样本获得 y(x)的积分值，并通过使用该方法获得复合辛普森规则。

```py
# import numpy and scipy.integrate
import numpy as np
from scipy import integrate

x = np.arange(0, 10)
y = np.arange(0, 10)
# using scipy.integrate.simps() method
gfg = integrate.simps(y, x)

print(gfg)
```

**输出:**

> Forty point five

**例 2 :**

```py
# import numpy and scipy.integrate
import numpy as np
from scipy import integrate

x = np.arange(0, 10)
y = np.sqrt(x)
# using scipy.integrate.simps() method
gfg = integrate.simps(y, x)

print(gfg)
```

**输出:**

> 17.875036119764566