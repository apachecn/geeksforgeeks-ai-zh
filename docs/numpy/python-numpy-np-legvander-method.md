# Python | Numpy np.legvander()方法

> 原文:[https://www . geesforgeks . org/python-numpy-NP-legvander-method/](https://www.geeksforgeeks.org/python-numpy-np-legvander-method/)

`**np.legvander()**`方法用于返回度 deg 和样本点 x 的范德蒙矩阵。

> **语法:** `np.legvander(x, deg)`
> **参数:**
> **x:**【Array _ like】点的数组。数据类型被转换为 float64 或 complex128，这取决于是否有任何元素是复杂的。如果 x 是标量，它被转换成一维数组。
> **度:**【int】所得矩阵的度。
> 
> **返回:**返回具有大小即 array.size +(度+ 1)的矩阵。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`np.legvander()`方法，我们能够使用该方法获得伪范德蒙矩阵。

```py
# import numpy
import numpy as np
import numpy.polynomial.legendre as geek

# using np.legvander() method
ans = geek.legvander((1, 3, 5, 7), 2)

print(ans)
```

**输出:**

> [[ 1.1.1.】
> 【1。3.13.】
> 【1。5.37.】
> 【1。7.73.]]

**例 2 :**

```py
# import numpy
import numpy as np
import numpy.polynomial.legendre as geek

ans = geek.legvander((1, 2, 3, 4), 3)

print(ans)
```

**输出:**

> [[ 1.1.1.1.】
> 【1。2.5.5 17.】
> 【1。3.13.63.】
> 【1。4.23.5 154.]]