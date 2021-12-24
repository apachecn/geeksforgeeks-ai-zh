# Python | Numpy matrix . repeat()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-repeat/](https://www.geeksforgeeks.org/python-numpy-matrix-repeat/)

借助`**Numpy matrix.repeat()**`方法，我们可以从给定的矩阵中得到**重复的**值，并以一维数组的形式给出输出。

> **语法:** `matrix.repeat(count)`
> 
> **返回:** *返回重复值的一维矩阵*

**示例#1 :**
在这个示例中，我们可以看到，借助方法`matrix.repeat()`，我们能够从给定的矩阵中获得重复值。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1; 12, 3]')

# applying matrix.repeat() method
geeks = gfg.repeat(2)

print(geeks)
```

**Output:**

```
[[64 64  1  1 12 12  3  3]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, -9]')

# applying matrix.repeat() method
geeks = gfg.repeat(3)

print(geeks)
```

**Output:**

```
[[ 1  1  1  2  2  2  3  3  3  4  4  4  5  5  5  6  6  6  7  7  7  8  8  8
  -9 -9 -9]]

```