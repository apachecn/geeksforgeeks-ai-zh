# python | num py NP . herm mul()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-NP-hermmul 方法/

借助`**np.hermemul()**`方法，利用`np.hermemul()`方法可以得到两个 hermiteE 级数的乘法。

> **语法:** `np.hermemul(series1, series2)`
> **返回:**返回两个 hermiteE 级数的乘积。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.hermemul()`方法，我们能够用这个方法得到两个 hermiteE 级数的乘法。

```
# import numpy and hermemul
import numpy as np
from numpy.polynomial.hermite_e import hermemul

series1 = np.array([1, 2, 3, 4])
series2 = np.array([10, 11, 12, 13])

# using np.hermemul() method
gfg = hermemul(series1, series2)

print(gfg)
```

**输出:**

> [416\. 667\. 1354\. 632\. 574\. 87\. 52.]

**例 2 :**

```
# import numpy and hermemul
import numpy as np
from numpy.polynomial.hermite_e import hermemul

series1 = np.array([11, 22, 33, 44])
series2 = np.array([10, 11, 12, 13])

# using np.hermemul() method
gfg = hermemul(series1, series2)

print(gfg)
```

**输出:**

> [4576\. 7337\. 14894\. 6952\. 6314\. 957\. 572.]