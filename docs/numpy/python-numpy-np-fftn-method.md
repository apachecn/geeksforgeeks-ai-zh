# Python | Numpy np.fftn()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-np-fftn-method/](https://www.geeksforgeeks.org/python-numpy-np-fftn-method/)

借助`**np.fftn()**`方法，我们可以利用`np.fftn()`方法得到 N-D **傅里叶变换**。

> **语法:** `np.fftn(Array)`
> **返回:**返回一个 N-D 级数的傅里叶变换。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.fftn()`方法，我们能够通过使用这个方法得到傅立叶变换的 N-D 级数。

```py
# import numpy
import numpy as np

a = np.array([-1, 3, -4, 7, 0])
# using np.fftn() method
gfg = np.fft.fftn(a)

print(gfg)
```

**输出:**

> [ 5.+0.j-2.5+3.61246823j-2.5-12.22497744j-2.5+12.22497744j
> -2.5-3.61246823j】

**例 2 :**

```py
# import numpy
import numpy as np

a = np.array([[-5.5, 4.4, -6.6, 3.3, -7.7], [1.1, -3.3, 4.4, -7.7, 0]])
# using np.fftn() method
gfg = np.fft.fftn(a)

print(gfg)
```

**输出:**

> [-17.6+0 . j-1.1-9.6624249j-1.1-3.08018588j
> -1.1+3.08018588j-1.1+9.6624249j]
> [-6.6+0 . j-6.6-1.7149948j-6.6-29.97513624j
> -6