# Python | Numpy matrix .非零()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-nonzero/](https://www.geeksforgeeks.org/python-numpy-matrix-nonzero/)

借助`**Numpy matrix.nonzero()**`方法，我们可以从给定的矩阵中得到**非零**值的指标值。它总是给我们二维数组。

> **语法:** `matrix.nonzero()`
> 
> **返回:** *从给定矩阵返回非零的指标值*

**示例#1 :**
在这个示例中，我们可以看到，借助方法`matrix.nonzero()`，我们能够从给定的矩阵中获得非零的索引值。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1; 0, 3]')

# applying matrix.nonzero() method
geeks = gfg.nonzero()

print(geeks)
```

**Output:**

```
(array([0, 0, 1]), array([0, 1, 1]))

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[11, 0, 3; 34, 0, 65; 7, 68, 0]')

# applying matrix.nonzero() method
geeks = gfg.nonzero()

print(geeks)
```

**Output:**

```
(array([0, 0, 1, 1, 2, 2]), array([0, 2, 0, 2, 0, 1]))

```