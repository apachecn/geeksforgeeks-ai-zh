# Python | Numpy matrix . mean()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-mean/](https://www.geeksforgeeks.org/python-numpy-matrix-mean/)

借助`**Numpy matrix.mean()**`方法，我们可以从给定矩阵中得到**均值**值。

> **语法:** `matrix.mean()`
> 
> **返回:** *返回给定矩阵的平均值*

**示例#1 :**
在这个示例中，我们可以看到，借助方法`matrix.mean()`，我们能够从给定的矩阵中获得平均值。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1; 12, 3]')

# applying matrix.mean() method
geeks = gfg.mean()

print(geeks)
```

**Output:**

```py
20.0

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.mean() method
geeks = gfg.mean()

print(geeks)
```

**Output:**

```py
5.0

```