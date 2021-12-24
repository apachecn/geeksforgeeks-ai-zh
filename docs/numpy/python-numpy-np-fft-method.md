# Python | Numpy np.fft()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-np-fft-method/](https://www.geeksforgeeks.org/python-numpy-np-fft-method/)

借助`**np.fft()**`方法，利用`np.fft()`方法可以得到一维**傅里叶变换**。

> **语法:** `np.fft(Array)`
> **返回:**返回一系列傅立叶变换。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.fft()`方法，我们能够用这个方法得到傅里叶变换的级数。

```
# import numpy
import numpy as np

a = np.array([5, 4, 6, 3, 7])
# using np.fft() method
gfg = np.fft.fft(a)

print(gfg)
```

**输出:**

> [25.+0.j 1.11803399+1.08981379j-1.11803399+4.61652531j
> -1.11803399–4.61652531j 1.11803399–1.08981379j】

**例 2 :**

```
# import numpy
import numpy as np

a = np.array([-5.5, 4.4, -6.6, 3.3, -7.7])
# using np.fft() method
gfg = np.fft.fft(a)

print(gfg)
```

**输出:**

> [-12.1+0 . j-3.85–5.68870985j-3.85–16.52766106j
> -3.85+16.52766106j-3.85+5.68870985j]