# Python | Numpy matrix.ptp()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-ptp/](https://www.geeksforgeeks.org/python-numpy-matrix-ptp/)

借助`**Numpy matrix.ptp()**`方法，我们可以从给定的矩阵中得到 **peek-to-peek** 值，即**(最大值-最小值)**。

> **语法:** `matrix.ptp(axis)`
> 
> **返回:** *从给定矩阵返回对等值*

**示例#1 :**
在这个示例中，我们可以看到，借助方法`matrix.ptp()`，我们能够从给定的矩阵中获得 peek-to-peek 值。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1; 12, 3]')

# applying matrix.ptp() method
geeks = gfg.ptp(1)

print(geeks)
```

**Output:**

```
[[63]
 [ 9]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, -9]')

# applying matrix.ptp() method
geeks = gfg.ptp(0)

print(geeks)
```

**Output:**

```
[[ 6  6 15]]

```