# Python | Numpy.dsplit()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-dsplit-method/](https://www.geeksforgeeks.org/python-numpy-dsplit-method/)

借助`**Numpy.dsplit()()**`方法，我们可以用`Numpy.dsplit()()`方法得到数组的分裂维数。

> **语法:** `Numpy.dsplit(numpy.array(), split_size)`
> 
> **返回:**返回具有分裂维度的数组。

**示例#1 :**

在这个例子中，我们可以看到使用`Numpy.expand_dims()`方法，我们能够使用这个方法得到分裂的维度。

```py
# import numpy
import numpy as np

# using Numpy.dsplit() method
gfg = np.array([[1, 2, 5],
                [3, 4, 10],
                [5, 6, 15],
                [7, 8, 20]])

gfg = gfg.reshape(1, 2, 6)
print(gfg)

gfg = np.dsplit(gfg, 2)
print(gfg)
```

**输出:**

> [[[ 1 2 5 3 4 10]
> [ 5 6 15 7 8 20]]]
> 
> [数组([[ 1，2，5]，
> [ 5，6，15]])，
> 数组([[ 3，4，10]，
> [ 7，8，20]])]

**例 2 :**

```py
# import numpy
import numpy as np

# using Numpy.expand_dims() method
gfg = np.array([[1, 2], [7, 8], [5, 10]])
gfg = gfg.reshape(1, 2, 3)
print(gfg)

gfg = np.dsplit(gfg, 3)
print(gfg)
```

**输出:**

> [[[ 1 2 7]
> [ 8 5 10]]]
> 
> [数组([[1]，
> [8]])，数组([[2]，
> [5]])，数组([[ 7]，
> [10]])]