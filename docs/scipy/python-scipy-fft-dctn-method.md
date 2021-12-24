# Python–scipy . FFT . dctn()方法

> 原文:[https://www.geeksforgeeks.org/python-scipy-fft-dctn-method/](https://www.geeksforgeeks.org/python-scipy-fft-dctn-method/)

借助 **scipy.fft.dctn()** 方法，我们可以通过选择不同类型的序列来计算多维离散余弦变换，并使用该方法返回变换后的数组。

**语法:**

```py
scipy.fft.dctn(x, type=2)

```

**返回值:**将返回变换后的数组。

**示例#1:** 在这个示例中，我们可以看到，通过使用 **scipy.fft.dctn()** 方法，我们能够通过选择不同类型的序列得到多维离散余弦变换，默认为 2。

## 蟒蛇 3

```py
# import scipy and numpy
from scipy import fft
import numpy as np

array_gfg = np.random.randn(3, 3)

# Using scipy.fft.dctn() method
gfg = fft.dctn(array_gfg)

print(gfg)
```

**输出:**

```py
[[ -4.16635907  -4.02741393  -3.60128725]
 [ -4.53247906  -3.48696887   0.9338914 ]
 [-10.02597376  -5.30097223   6.56879818]]

```

**例 2:**

## 蟒蛇 3

```py
# import scipy and numpy
from scipy import fft
import numpy as np

array_gfg = np.random.randn(5, 5)

# Using scipy.fft.dctn() method
gfg = fft.dctn(array_gfg, 1)

print(gfg)
```

**输出:**

```py
[[-22.58866562   4.34759109   6.27133607 -10.09673997   1.42277882]
 [-10.38551445  -1.73284723   4.77719083  -8.1483736    2.31129559]
 [  5.09865556   7.7860346   -1.99346709  -8.19680308   5.54398566]
 [ 11.03512166 -13.2738255   -6.30390925   5.55873569  -3.67046116]
 [ 11.70752959 -13.28207081   6.20179649  11.0564309    5.17738824]]

```