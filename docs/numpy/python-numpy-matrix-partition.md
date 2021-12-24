# Python | Numpy matrix . partition()

> 原文:[https://www . geesforgeks . org/python-numpy-matrix-partition/](https://www.geeksforgeeks.org/python-numpy-matrix-partition/)

借助`**Numpy matrix.partition()**`方法，我们能够以这样的方式划分矩阵:我们传递的索引值对矩阵进行排序，就像所有小于该值的值都向左移动一样，而其他值在`matrix.partition()`方法的帮助下向右移动。

> **语法:** `matrix.partition(index)`
> 
> **返回:** *返回分区矩阵*

**示例#1 :**
在这个示例中，我们可以看到，我们能够借助方法`matrix.partition()`对给定的矩阵进行划分。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1, 12, 3]')

# applying matrix.partition() method
gfg.partition(3)

print(gfg)
```

**Output:**

```
[[ 1  3 12 64]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[11, 29, 3, 44, 25, 16, 71, 8, 19]')

# applying matrix.partition() method
gfg.partition(3)

print(gfg)
```

**Output:**

```
[[ 3  8 11 16 19 25 29 44 71]]

```