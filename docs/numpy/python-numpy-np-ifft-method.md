# Python | Numpy np.ifft()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-np-ifft-method/](https://www.geeksforgeeks.org/python-numpy-np-ifft-method/)

借助`**np.ifft()**`方法，利用`np.ifft()`方法可以得到一维**傅里叶逆变换**。

> **语法:** `np.ifft(Array)`
> **返回:**返回一系列傅里叶逆变换。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.ifft()`方法，我们能够用这个方法得到傅里叶逆变换的级数。

```py
# import numpy
import numpy as np

a = np.array([5, 4, 6, 3, 7])
# using np.ifft() method
gfg = np.fft.ifft(a)

print(gfg)
```

**输出:**

> [ 5.+0.j 0.2236068–0.21796276j-0.2236068–0.92330506j
> -0.2236068+0.92330506j 0.2236068+0.21796276j】

**例 2 :**

```py
# import numpy
import numpy as np

a = np.array([-5.5, 4.4, -6.6, 3.3, -7.7])
# using np.ifft() method
gfg = np.fft.ifft(a)

print(gfg)
```

**输出:**

> [-2.42+0 . j-0.77+1.13774197j-0.77+3.3055321j-0.77–3.3055321j
> -0.77–1.13774197j]