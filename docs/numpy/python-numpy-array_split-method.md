# Python | numpy.array_split()方法

> 原文:[https://www . geesforgeks . org/python-numpy-array _ split-method/](https://www.geeksforgeeks.org/python-numpy-array_split-method/)

借助`**numpy.array_split()**`方法，我们可以用`numpy.array_split()`方法得到不同维数的分裂数组。

> **语法:** `numpy.array_split()`
> 
> **返回:**返回一维的分裂数组。

**示例#1 :**
在这个示例中，我们可以看到，通过使用`numpy.array_split()`方法，我们能够通过将数组作为参数传递来拆分数组中的子数组数量。

```
# import numpy
import numpy as np

array = np.arange(9)

# using numpy.array_split() method
gfg = np.array_split(array, 4)

print(gfg)
```

**输出:**

> [数组([0，1，2])，数组([3，4])，数组([5，6])，数组([7，8])]

**例 2 :**

```
# import numpy
import numpy as np

array = [[1, 2, 3],
         [4, 5, 6],
         [7, 8, 9]]

# using numpy.array_split() method
gfg = np.array_split(array, 3)

print(gfg)
```

**输出:**

> [数组([[1，2，3]])，数组([[4，5，6]])，数组([[7，8，9]])]