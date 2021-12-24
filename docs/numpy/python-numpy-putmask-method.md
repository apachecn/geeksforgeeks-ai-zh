# Python | numpy.putmask()方法

> 原文:[https://www.geeksforgeeks.org/python-numpy-putmask-method/](https://www.geeksforgeeks.org/python-numpy-putmask-method/)

借助`**numpy.putmask()**`方法，我们可以利用`numpy.putmask()`方法，借助条件和给定值来改变数组中的元素。

> **语法:** `numpy.putmask(array, condition, value)`
> **返回:**根据值返回有新元素的数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`numpy.putmask()`方法，我们能够在给定条件和值的帮助下获得新数组。

```py
# import numpy
import numpy as np

# using numpy.putmask() method
arr = np.array([1, 2, 3, 4, 5, 6])
np.putmask(arr, arr % 2 == 0, 0)

print(arr)
```

**输出:**

> 数组([1，0，3，0，5，0])

**例 2 :**

```py
# import numpy
import numpy as np

# using numpy.putmask() method
arr = np.array([[1, 2, 3],
                [3, 2, 1],
                [1, 2, 3]])

np.putmask(arr, arr>2, 4)

print(arr)
```

**输出:**

> [[1 2 4]
> [4 2 1]
> [1 2 4]]