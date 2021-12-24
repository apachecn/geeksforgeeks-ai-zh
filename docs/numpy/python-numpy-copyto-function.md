# Python | numpy.copyto()函数

> 原文:[https://www.geeksforgeeks.org/python-numpy-copyto-function/](https://www.geeksforgeeks.org/python-numpy-copyto-function/)

借助`**Numpy numpy.copyto()**`方法，我们可以复制 numpy 数组中存在的所有数据元素。如果我们更改副本中的任何数据元素，它将不会影响原始 numpy 数组。

> **语法:** `numpy.copyto(destination, source)`
> 
> **返回:** *返回数组副本*

**示例#1 :**
在这个示例中，我们可以看到借助于`numpy.copyto()`方法，我们正在复制目标数组中的元素。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([1, 2, 3])
geeks = [4, 5, 6]

# applying numpy.copyto() method
np.copyto(gfg, geeks)

print(gfg)
```

**Output:**

```py
[4 5 6]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.array([[1, 2, 3], [4, 5, 6]])
geeks = [[4, 5, 6], [7, 8, 9]]

# applying numpy.copyto() method
np.copyto(gfg, geeks)

print(gfg)
```

**Output:**

```py
[[4 5 6]
 [7 8 9]]

```