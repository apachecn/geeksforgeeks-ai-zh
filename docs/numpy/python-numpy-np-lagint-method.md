# Python | Numpy np.lagint()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag int-method/](https://www.geeksforgeeks.org/python-numpy-np-lagint-method/)

借助`**np.lagint()**`方法，利用`np.lagint()`方法可以得到阵列形式的拉盖尔级数。

> **语法:** `np.lagint(array of coefficient)`
> **回礼:**回礼拉盖尔系列之阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.lagint()`方法，我们能够以数组的形式获得拉盖尔级数。

```
# import numpy
from numpy.polynomial.laguerre import lagint

# using np.lagint() method
gfg = lagint([1, 2, 3])

print(gfg)
```

**输出:**

> [ 1\. 1\. 1\. -3.]

**例 2 :**

```
# import numpy
from numpy.polynomial.laguerre import lagint

# using np.lagint() method
gfg = lagint([[1, 2, 3], [4, 5, 6]])

print(gfg)
```

**输出:**

> [[ 1.2.3.】
> 【3。3.3.】
> 【-4。-5.-6.]]