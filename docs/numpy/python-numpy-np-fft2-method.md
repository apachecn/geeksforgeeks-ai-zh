# Python | Numpy np.fft2()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-np-fft2-method/](https://www.geeksforgeeks.org/python-numpy-np-fft2-method/)

借助`**np.fft2()**`方法，利用`np.fft2()`方法可以得到二维**傅里叶变换**。

> **语法:** `np.fft2(Array)`
> **返回:**返回一个 2-D 系列的傅立叶变换。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.fft2()`方法，我们能够使用该方法获得傅立叶变换的 2-D 系列。

```py
# import numpy
import numpy as np

a = np.array([[5, 4, 6, 3, 7], [-1, -3, -4, -7, 0]])
# using np.fft2() method
gfg = np.fft.fft2(a)

print(gfg)
```

**输出:**

> [[10.+0.j 8.09016994+2.17962758j-3.09016994+9.23305061j
> -3.09016994–9.23305061j 8.09016994–2.17962758j】
> 【40。+0 . j-5.85410197+0 . j 0.85410197+0 . j
> 0.85410197+0 . j-5.85410197+0 . j]]

**例 2 :**

```py
# import numpy
import numpy as np

a = np.array([[-5.5, 4.4, -6.6, 3.3, -7.7], [1.1, -3.3, 4.4, -7.7, 0]])
# using np.fft2() method
gfg = np.fft.fft2(a)

print(gfg)
```

**输出:**

> 【-17.6+0 . j-1.1–9.6624249j-1.1–3.08018588j
> -1.1+3.08018588j-1.1+9.6624249j】
> 【-6.6+0 . j-6.6–1.7149948j-6.6–29.97513624j
> -6