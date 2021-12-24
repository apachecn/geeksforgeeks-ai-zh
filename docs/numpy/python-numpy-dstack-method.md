# Python | Numpy dstack()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-dstack-method/](https://www.geeksforgeeks.org/python-numpy-dstack-method/)

借助`**numpy.dstack()**`方法，我们可以通过索引得到组合数组索引，并通过`numpy.dstack()`方法像堆栈一样存储。

> **语法:** `numpy.dstack((array1, array2))`
> 
> **返回:**按索引返回组合数组索引。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`numpy.dstack()`方法，我们能够逐个索引地获得堆栈索引中的组合数组。

```py
# import numpy
import numpy as np

gfg1 = np.array([1, 2, 3])
gfg2 = np.array([4, 5, 6])

# using numpy.dstack() method
print(np.dstack((gfg1, gfg2)))
```

**输出:**

> [[[1 4]
> [2 5]
> [3 6]]]

**例 2 :**

```py
# import numpy
import numpy as np

gfg1 = np.array([[10], [2], [13]])
gfg2 = np.array([[41], [55], [6]])

# using numpy.dstack() method
print(np.dstack((gfg1, gfg2)))
```

**输出:**

> [[[10 41]]
> 
> [[ 2 55]]
> 
> [[13 6]]]