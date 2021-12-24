# Python–scipy . FFT . idst()方法

> 原文:[https://www.geeksforgeeks.org/python-scipy-fft-idst-method/](https://www.geeksforgeeks.org/python-scipy-fft-idst-method/)

借助 **scipy.fft.idst()** 方法，我们可以通过选择不同类型的序列来计算离散正弦变换的逆，并使用该方法返回变换后的数组。

**语法:**

```
scipy.fft.idst(x, type=2)

```

**返回值:**将返回变换后的数组。

**示例#1:** 在本例中，我们可以看到，通过使用 **scipy.fft.idst()** 方法，我们能够通过选择不同类型的序列来获得离散正弦变换的逆，默认为 2。

## 蟒 3

```
# import scipy
from scipy import fft

# Using scipy.fft.idst() method
gfg = fft.idst([1, 2, 3, 4])

print(gfg)
```

**输出:**

```
[ 1.6421339  -0.2024893   0.09040392 -0.06497288]

```

**例 2 :**

## 蟒 3

```
# import scipy
from scipy import fft

# Using scipy.fft.idst() method
gfg = fft.idst([-6, 5, -4, 3, -2, 1], 3)

print(gfg)
```

**输出:**

```
[-0.02311678  0.00 -0.11785113  0.000 -1.20162809 -3.5]

```