# python 中的 scipy.rfft()

> 原文:[https://www.geeksforgeeks.org/scipy-rfft-in-python/](https://www.geeksforgeeks.org/scipy-rfft-in-python/)

借助 **scipy.rfft()** 方法，我们可以计算实序列的快速傅里叶变换，并使用该方法返回变换后的向量。

> **语法:** scipy.fft.rfft(x)
> 
> **返回:**返回转换后的向量。

**示例#1 :**

在这个例子中我们可以看到，通过使用 **scipy.rfft()** 方法，我们能够计算实序列的快速傅立叶变换，并通过使用该方法返回变换后的向量。

## 蟒蛇 3

```py
# import scipy and numpy
import scipy
import numpy as np

x = np.arange(5)
# Using scipy.fftfreq() method
gfg = scipy.fft.rfft(x)

print(gfg)
```

**输出:**

> [10.+0 . j-2.5+3.4409548j-2.5+0.81229924j]

**例 2 :**

## 蟒蛇 3

```py
# import scipy and numpy
import scipy
import numpy as np

x = np.arange(10)
# Using scipy.fftfreq() method
gfg = scipy.fft.rfft(x)

print(gfg)
```

**输出:**

> [45.+0.j -5。+15.38841769j -5。+6.8819096j -5。+3.63271264j
> 
> -5.+1.62459848j -5。+0.j ]