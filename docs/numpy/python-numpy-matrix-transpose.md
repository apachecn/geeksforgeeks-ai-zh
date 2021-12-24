# Python | Numpy matrix .转置()

> 原文:[https://www . geeksforgeeks . org/python-numpy-matrix-transpose/](https://www.geeksforgeeks.org/python-numpy-matrix-transpose/)

借助`**Numpy matrix.transpose()**`方法，我们可以用`matrix.transpose()`方法求出矩阵的转置。

> **语法:** `matrix.transpose()`
> **返回:** **返回转置矩阵**

**示例#1 :**
在这个示例中，我们可以看到，通过使用`**matrix.transpose()**`方法，我们能够找到给定矩阵的转置。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1; 12, 3]')

# applying matrix.transpose() method
geek = gfg.transpose()

print(geek)
```

**Output:**

```
[[ 4 12]
 [ 1  3]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.transpose() method
geek = gfg.transpose()

print(geek)
```

**Output:**

```
[[ 4 12  4]
 [ 1  3  5]
 [ 9  1  6]]

```