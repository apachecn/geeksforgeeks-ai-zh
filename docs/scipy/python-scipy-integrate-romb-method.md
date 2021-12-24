# Python | Scipy integrate.romb()方法

> 原文:[https://www . geesforgeks . org/python-scipy-integrate-romb-method/](https://www.geeksforgeeks.org/python-scipy-integrate-romb-method/)

借助`**scipy.integrate.romb()**`方法，我们可以利用`scipy.integrate.romb()`方法，利用函数从极限 a 到极限 b 的样本，得到龙贝格积分。

> **语法:** `scipy.integrate.romb(y, dx, axis, show)`
> **返回:**返回龙贝格积分的一个样本。

**示例#1 :**
在本例中，我们可以看到，通过使用`scipy.integrate.romb()`方法，我们能够通过使用该方法使用从极限 a 到极限 b 的函数样本来获得龙贝格积分。

```py
# import numpy and scipy.integrate
import numpy as np
from scipy import integrate
x = np.arange(3, 12)

# using scipy.integrate.romb() method
gfg = integrate.romb(x)

print(gfg)
```

**输出:**

> Fifty-six

**例 2 :**

```py
# import numpy and scipy.integrate
import numpy as np
from scipy import integrate
x = np.arange(3, 12)
y = np.cos(np.power(x, 3.5))

# using scipy.integrate.romb() method
gfg = integrate.romb(y)

print(gfg)
```

**输出:**

> -3.5943771512643674