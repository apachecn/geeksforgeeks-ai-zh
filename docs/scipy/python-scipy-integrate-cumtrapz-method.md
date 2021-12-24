# Python | Scipy integral . cum trapz()方法

> 原文:[https://www . geesforgeks . org/python-scipy-integrate-cum trapz-method/](https://www.geeksforgeeks.org/python-scipy-integrate-cumtrapz-method/)

借助`scipy.integrate.cumtrapz()`方法，利用`scipy.integrate.cumtrapz()`方法，利用复合梯形法则可以得到 y(x)的累积积分值。

> **语法:** `scipy.integrate.cumtrapz()`
> **返回:**返回 y(x)的累计积分值。

**例#1 :**
在这个例子中我们可以看到，通过使用`scipy.integrate.cumtrapz()`方法，我们能够通过使用该方法获得使用梯形规则的 y(x)的累积积分。

```
# import numpy and scipy.integrate.cumtrapz
import numpy as np
from scipy import integrate

x = np.arange(0, 10)
y = np.arange(0, 10)
# using scipy.integrate.cumtrapz() method
gfg = integrate.cumtrapz(y, x)

print(gfg)
```

**输出:**

> [0.5 2\. 4.5 8\. 12.5 18\. 24.5 32\. 40.5]

**例 2 :**

```
# import numpy and scipy.integrate.cumtrapz
import numpy as np
from scipy import integrate

x = np.arange(0, 10)
y = np.power(x, 2)
# using scipy.integrate.cumtrapz() method
gfg = integrate.cumtrapz(y, x)

print(gfg)
```

**输出:**

> [0.5 3\. 9.5 22\. 42.5 73\. 115.5 172\. 244.5]