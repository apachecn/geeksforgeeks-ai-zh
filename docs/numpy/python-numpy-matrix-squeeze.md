# Python | Numpy matrix . crunch()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-squeeze/](https://www.geeksforgeeks.org/python-numpy-matrix-squeeze/)

借助`**matrix.squeeze()**`方法，我们可以用同样的方法挤压出矩阵的大小。但是记住一件事，我们在 **Nx1** 矩阵的大小上使用这种方法，它给出为 **1xN** 矩阵。

> **语法:** `matrix.squeeze()`
> **返回:**返回一个压缩矩阵

**示例#1 :**
在本例中，我们可以使用`matrix.squeeze()`方法来挤压给定矩阵的大小。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[[4], [12]]')

# applying matrix.squeeze() method
gfg.squeeze()

print(gfg)
```

**Output:**

```
[[ 4 12]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.squeeze() method
gfg.squeeze()

print(gfg)
```

**Output:**

```
[[ 4  1  9]
 [12  3  1]
 [ 4  5  6]]

```