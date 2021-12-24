# Python | Numpy matrix . copy()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-copy/](https://www.geeksforgeeks.org/python-numpy-matrix-copy/)

借助`**Numpy matrix.copy()**`方法，我们可以复制矩阵中存在的所有数据元素。如果我们更改副本中的任何数据元素，它将不会影响原始矩阵。

> **语法:** `matrix.copy()`
> 
> **返回:** *返回矩阵副本*

**示例#1 :**
在这个示例中，我们可以看到借助于`matrix.copy()`方法，我们正在不同矩阵中复制一个元素。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[1, 2, 3]')

# applying matrix.copy() method
geeks = gfg.copy()

print(geeks)
```

**Output:**

```
[[1 2 3]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6]')

# applying matrix.copy() method
geeks = gfg.copy()

print(geeks)
```

**Output:**

```
[[1 2 3]
 [4 5 6]]

```