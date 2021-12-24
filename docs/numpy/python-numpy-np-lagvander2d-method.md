# Python | Numpy np.lagvander2d()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-lagvander2d-method/](https://www.geeksforgeeks.org/python-numpy-np-lagvander2d-method/)

借助于`**np.lagvander2d()**`方法，我们可以从给定的数组中得到伪范德蒙矩阵，通过`np.lagvander2d()`方法将该矩阵作为参数传递。

> **语法:** `np.lagvander2d(x, y, deg)`
> **参数:**
> **x，y:**【Array _ like】点的数组。数据类型被转换为 float64 或 complex128，这取决于是否有任何元素是复杂的。如果 x 是标量，它被转换成一维数组
> **度:**【int】所得矩阵的度数。
> 
> **返回:**返回具有大小即 array.size +(度+ 1)的矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.lagvander2d()`方法，我们能够使用该方法获得伪范德蒙矩阵。

```py
# import numpy
import numpy as np
import numpy.polynomial.laguerre as geek

# using np.lagvander() method
ans = geek.lagvander2d((1, 3, 5, 7), (2, 4, 6, 8), [2, 2])

print(ans)
```

**输出:**

> [[ 1.-1.-1.0.-0.-0.-0.5 0.5 0.5]
> 【1。-3.1.-2.6.-2.-0.5 1.5-0.5]
> 【1。-5.7.-4.20.-28.3.5-17.5 24.5]
> 【1。-7.17.-6.42.-102.11.5 -80.5 195.5]]

**例 2 :**

```py
# import numpy
import numpy as np
import numpy.polynomial.laguerre as geek

ans = geek.lagvander2d((1, 2, 3, 4), (5, 6, 7, 8), [3, 3])

print(ans)
```

**输出:**

> [[ 1.-4.3.5 2.66666667 0.-0.
> 0。0.-0.5 2.-1.75-1.33333333
> -0.6666667 2.666667-2.33333333-1.777778】
> 【1。-5.7.1.-1.5.
> -7。-1.-1.5.-7.-1.
> -0.33333333 1.6666667-2.33333333-0.3333333】
> 【1。-6.11.5 -3.66666667 -2.12.
> -23。7.33333333 -0.5 3.-5.75 1.83333333
> 1。-6.11.5-3.6666667]
> 【1。-7.17.-12.33333333 -3.21.
> -51。37.1.-7.17.-12.3333333
> 2.333333333-16.33333339.6666667-28.7777778]]