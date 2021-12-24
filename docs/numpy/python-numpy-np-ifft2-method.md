# Python | Numpy np.ifft2()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-np-ifft2-method/](https://www.geeksforgeeks.org/python-numpy-np-ifft2-method/)

借助`**np.ifft2()**`方法，利用`np.ifft2()`方法可以得到二维**傅里叶逆变换**。

> **语法:** `np.fft2(Array)`
> **返回:**返回一个 2-D 级数的傅里叶逆变换。

**示例#1 :**
在这个示例中我们可以看到，通过使用`np.ifft2()`方法，我们能够通过使用该方法获得傅里叶逆变换的 2-D 系列。

```py
# import numpy
import numpy as np

a = np.array([[5, 4, 6, 3, 7], [-1, -3, -4, -7, 0]])
# using np.ifft2() method
gfg = np.fft.ifft2(a)

print(gfg)
```

**输出:**

> [[ 1.+0.j 0.80901699-0.21796276j-0.30901699-0.92330506j
> -0.30901699+0.92330506j 0.80901699+0.21796276j】
> 【4。+0 . j-0.5854102+0 . j 0.0854102+0 . j
> 0.0854102+0 . j-0.5854102+0 . j]]

**例 2 :**

```py
# import numpy
import numpy as np

a = np.array([[-5.5, 4.4, -6.6, 3.3, -7.7], [1.1, -3.3, 4.4, -7.7, 0]])
# using np.ifft2() method
gfg = np.fft.ifft2(a)

print(gfg)
```

**输出:**

> [-1.76+0 . j-0.11+0.96624249j-0.11+0.30801859j-0.11-0.30801859j
> -0.11-0.96624249j]
> [-0.66+0.j-0.66+0.17149948j-0.66+2.99751515