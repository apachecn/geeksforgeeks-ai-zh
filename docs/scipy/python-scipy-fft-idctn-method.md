# Python–scipy . FFT . idctn()方法

> 原文:[https://www . geesforgeks . org/python-scipy-FFT-idctn-method/](https://www.geeksforgeeks.org/python-scipy-fft-idctn-method/)

借助 **scipy.fft.idctn()** 方法，我们可以通过选择不同类型的序列来计算多维离散余弦变换的逆，并使用该方法返回变换后的数组。

**语法:**

```py
scipy.fft.idctn(x, type=2)

```

**返回值:**将返回变换后的数组。

**示例#1:** 在这个示例中，我们可以看到，通过使用 scipy.fft.idctn()方法，我们能够通过选择不同类型的序列来获得多维离散余弦变换的逆，默认为 2。

## 蟒蛇 3

```py
# import scipy and numpy
from scipy import fft
import numpy as np

array_gfg = np.random.randn(3, 3)

# Using scipy.fft.idctn() method
gfg = fft.idctn(array_gfg)

print(gfg)
```

**输出:**

```py
[[-0.27264259  0.12356192  0.12133914]
 [ 0.00835797  0.11993761 -0.12110712]
 [ 0.09770593 -0.14543749 -0.01109258]]

```

**例 2 :**

## 蟒蛇 3

```py
# import scipy and numpy
from scipy import fft
import numpy as np

array_gfg = np.random.randn(4, 2)

# Using scipy.fft.idctn() method
gfg = fft.idctn(array_gfg, 4)

print(gfg)
```

**输出:**

```py
[[ 0.1430296   0.09689253]
 [ 0.00632705  0.24546606]
 [-0.26553743  0.01931002]
 [-0.07106229 -0.02292552]]

```