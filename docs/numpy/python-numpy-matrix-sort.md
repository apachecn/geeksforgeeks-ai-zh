# Python | Numpy matrix . sort()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-sort/](https://www.geeksforgeeks.org/python-numpy-matrix-sort/)

借助`**matrix.sort()**`方法，我们可以用同样的方法对矩阵中的值进行排序。

> **语法:** `matrix.sort()`
> **返回:**返回排序后的矩阵

**示例#1 :**
在本例中，我们能够使用`matrix.sort()`方法对矩阵中的元素进行排序。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1; 12, 3]')

# applying matrix.sort() method
gfg.sort()

print(gfg)
```

**Output:**

```py
[[ 1  4]
 [ 3 12]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.sort() method
gfg.sort()

print(gfg)
```

**Output:**

```py
[[ 1  4  9]
 [ 1  3 12]
 [ 4  5  6]]

```