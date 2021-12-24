# Python–scipy . FFT . IDCT()方法

> 原文:[https://www.geeksforgeeks.org/python-scipy-fft-idct-method/](https://www.geeksforgeeks.org/python-scipy-fft-idct-method/)

借助 **scipy.fft.idct()** 方法，我们可以通过选择不同类型的序列来计算逆离散余弦变换，并使用该方法返回变换后的数组。

![](img/d9c81adec0a702c9b81fb8e35b6b1233.png)

**语法:**

```py
scipy.fft.idct(x, type=2)

```

**返回值:**将返回逆变换后的数组。

**示例#1:** 在这个示例中，我们可以看到，通过使用 scipy.fft.idct()方法，我们能够通过选择不同类型的序列来获得逆离散余弦变换，默认为 2。

## 蟒蛇 3

```py
# import scipy
from scipy import fft

# Using scipy.fft.idct() method
gfg = fft.idct([0.1, 2.1, 0.3, 4.2])

print(gfg)
```

**输出:**

```py
[ 0.95238737 -0.80969772  0.7286317  -0.82132135]

```

**例 2:**

## 蟒蛇 3

```py
# import scipy
from scipy import fft

# Using scipy.fft.idct() method
gfg = fft.idct([0.95238737, -0.80969772, 0.7286317, -0.82132135], 4)

print(gfg)
```

**输出:**

```py
[0.12635568 0.17287895 0.19562573 0.51175513]

```