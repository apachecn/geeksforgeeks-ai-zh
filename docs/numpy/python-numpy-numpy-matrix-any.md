# python | num py . matrix . any()

> 原文:[https://www . geeksforgeeks . org/python-numpy-numpy-matrix-any/](https://www.geeksforgeeks.org/python-numpy-numpy-matrix-any/)

借助`**Numpy numpy.matrix.any()**`方法，我们可以将一个矩阵的每个元素与另一个进行比较，或者我们可以提供我们想要应用比较的轴，如果有任何元素匹配，则返回 true。

> **语法:** `numpy.matrix.any()`
> 
> **返回:** *如果发现匹配，返回真，否则返回假*

**示例#1 :**
在这个示例中，我们可以看到借助于`matrix.any()`方法，我们能够比较任何两个具有不同维度的矩阵，如果找到任何匹配，则返回 true。

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg1 = np.matrix('[1, 2, 3, 4]')
gfg2 = np.matrix('[1, 2]')

# applying matrix.any() method
geeks = (gfg1 == gfg2).any()

print(geeks)
```

**Output:**

```py
True

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg1 = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')
gfg2 = np.matrix('[1, 2, 3]')

# applying matrix.any() method
geeks = (gfg1 == gfg2).any()

print(geeks)
```

**Output:**

```py
True

```