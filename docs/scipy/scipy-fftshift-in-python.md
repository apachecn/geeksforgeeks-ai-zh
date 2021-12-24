# Python 中的 scipy.fftshift()

> 原文:[https://www.geeksforgeeks.org/scipy-fftshift-in-python/](https://www.geeksforgeeks.org/scipy-fftshift-in-python/)

借助**scipy . fftsshift()**方法，我们可以利用快速傅里叶变换对向量的上半部分和下半部分进行移位，并利用该方法返回移位后的向量。

> **语法:** scipy.fft.fftshift(x)
> 
> **返回:**返回转换后的向量。

**示例#1 :**

在这个例子中我们可以看到，通过使用**scipy . fftsshift()**方法，我们能够通过使用快速傅立叶变换来移位向量的下半部分和上半部分，并返回移位的向量。

## 蟒蛇 3

```
# import scipy and numpy
import scipy
import numpy as np

x = np.arange(6)
# Using scipy.fftfreq() method
gfg = scipy.fft.fftshift(x)

print(gfg)
```

**输出:**

> [3 4 5 0 1 2]

**例 2 :**

## 蟒蛇 3

```
# import scipy and numpy
import scipy
import numpy as np

x = np.arange(11)
# Using scipy.fftfreq() method
gfg = scipy.fft.fftshift(x)

print(gfg)
```

**输出:**

> [ 6  7  8  9 10  0  1  2  3  4  5]