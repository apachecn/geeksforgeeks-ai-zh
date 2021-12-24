# scipy.fftfreq()用 Python

表示

> 原文:[https://www.geeksforgeeks.org/scipy-fftfreq-in-python/](https://www.geeksforgeeks.org/scipy-fftfreq-in-python/)

借助 **scipy.fftfreq()** 方法，我们可以计算快速傅里叶变换频率，并使用该方法返回变换后的数组。

> **语法:** scipy.fftfreq(n，freq)
> 
> **返回:**返回变换后的数组。

**示例#1 :**

在这个例子中我们可以看到，通过使用 **scipy.fftfreq()** 方法，我们能够计算快速傅立叶变换频率并返回变换后的数组。

## 蟒蛇 3

```py
# import scipy and numpy
import scipy
import numpy as np

# Using scipy.fftfreq() method
gfg = scipy.fft.fftfreq(5, 1.096)

print(gfg)
```

**输出:**

> [ 0\.          0.18248175  0.3649635  -0.3649635  -0.18248175]

**例 2 :**

## 蟒蛇 3

```py
# import scipy and numpy
import scipy
import numpy as np

# Using scipy.fftfreq() method
gfg = scipy.fft.fftfreq(3, 2.4096)

print(gfg)
```

**输出:**

> [ 0\.          0.13833555 -0.13833555]