# Python | Numpy np.lagvander()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lag Vander-method/](https://www.geeksforgeeks.org/python-numpy-np-lagvander-method/)

借助于`**np.lagvander()**`方法，我们可以从给定的数组中得到伪范德蒙矩阵，通过`np.lagvander()`方法将该矩阵作为参数传递。

> **语法:** `np.lagvander(arr, degree)`
> **参数:**
> **arr:**【Array _ like】点的数组。数据类型被转换为 float64 或 complex128，这取决于是否有任何元素是复杂的。如果 x 是标量，它被转换成一维数组
> **度:**【int】所得矩阵的度数。
> 
> **返回:**返回具有大小即 array.size +(度+ 1)的矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.lagvander()`方法，我们能够使用该方法获得伪范德蒙矩阵。

```py
# import numpy
import numpy as np
import numpy.polynomial.laguerre as geek

# using np.lagvander() method
gfg = geek.lagvander((1, 3, 5, 7), 2)

print(gfg)
```

**输出:**

> [[ 1.0.-0.5]
> 【1。-2.-0.5]
> 【1。-4.3.5】
> 【1。-6.11.5]]

**例 2 :**

```py
# import numpy
import numpy as np
import numpy.polynomial.laguerre as geek

# using np.lagvander() method
gfg = geek.lagvander((2, 5, 1, 12), 5)

print(gfg)
```

**输出:**

> [[ 1.-1.-1.-0.33333333 0.33333333
> 0.73333333】
> 【1。-4.3.5 2.6666667-1.29166667
> -3.1666667】
> 【1。0.-0.5-0.6666667-0.625
> -0.4666667】
> 【1。-11.49.-107.97.27.4 ]]