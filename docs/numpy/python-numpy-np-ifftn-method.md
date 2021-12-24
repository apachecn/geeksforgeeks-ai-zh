# Python | Numpy np.ifftn()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-np-ifftn-method/](https://www.geeksforgeeks.org/python-numpy-np-ifftn-method/)

借助`**np.ifftn()**`方法，利用`np.fftn()`方法可以得到 N-D **逆傅里叶变换**。

> **语法:** `np.ifftn(Array)`
> 
> **返回:**返回傅里叶逆变换的 N-D 级数。

**例#1 :**
在这个例子中我们可以看到，通过使用`np.ifftn()`方法，我们能够通过使用这个方法得到傅里叶逆变换的 N-D 级数。

```py
# import numpy
import numpy as np

a = np.array([-1, 3, -4, 7, 0])

# using np.ifftn() method
gfg = np.fft.ifftn(a)

print(gfg)
```

**输出:**

> [ 1.+0.j-0.5-0.72249365j-0.5+2.44499549j-0.5-2.44499549j
> -0.5+0.72249365j】

**例 2 :**

```py
# import numpy
import numpy as np

a = np.array([[-5.5, 4.4, -6.6, 3.3, -7.7], [1.1, -3.3, 4.4, -7.7, 0]])

# using np.ifftn() method
gfg = np.fft.ifftn(a)

print(gfg)
```

**输出:**

> [-1.76+0 . j-0.11+0.96624249j-0.11+0.30801859j-0.11-0.30801859j
> -0.11-0.96624249j]
> [-0.66+0.j-0.66+0.17149948j-0.66+2.99751515