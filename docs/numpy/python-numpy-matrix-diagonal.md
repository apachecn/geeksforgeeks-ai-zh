# Python | Numpy matrix .对角线()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-diagonal/](https://www.geeksforgeeks.org/python-numpy-matrix-diagonal/)

借助`**Numpy matrix.diagonal()**`方法，我们能够从给定的矩阵中找到一个`diagonal element`，并以一维矩阵的形式给出输出。

> **语法:** `matrix.diagonal()`
> 
> **返回:** *返回矩阵的对角元素*

**示例#1 :**
在这个示例中，我们可以看到借助于`matrix.diagonal()`方法，我们能够找到矩阵对角线上的元素。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6, 2; 3, 4]')

# applying matrix.diagonal() method
geeks = gfg.diagonal()

print(geeks)
```

**Output:**

```
[[6 4]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.diagonal() method
geeks = gfg.diagonal()

print(geeks)
```

**Output:**

```
[[1 5 9]]

```