# Python | Numpy matrix.put()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-put/](https://www.geeksforgeeks.org/python-numpy-matrix-put/)

借助`**Numpy matrix.put()**`方法，我们可以通过传递给定矩阵中的索引和值来将**值**放入。

> **语法:** `matrix.put(index, value)`
> 
> **返回:** *返回新矩阵*

**示例#1 :**
在这个示例中，我们可以看到，借助方法`matrix.put()`，我们可以将中的值放入给定的矩阵中。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1; 12, 3]')

# applying matrix.put() method
gfg.put((0, 1), 45)

print(gfg)
```

**Output:**

```py
[[45 45]
 [12  3]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, -9]')

# applying matrix.put() method
gfg.put(2, 43)

print(gfg)
```

**Output:**

```py
[[ 1  2 43]
 [ 4  5  6]
 [ 7  8 -9]]

```