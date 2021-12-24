# Python | Numpy matrix . ravel()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-matrix-ravel/

借助`**Numpy matrix.ravel()**`方法，我们可以从给定的矩阵中得到**展平的**矩阵。

> **语法:** `matrix.ravel()`
> 
> **返回:** *从给定矩阵返回扁平矩阵*

**示例#1 :**
在这个示例中，我们可以看到，借助方法`matrix.ravel()`，我们能够从给定的矩阵中获得展平的矩阵。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1; 12, 3]')

# applying matrix.ravel() method
geeks = gfg.ravel()

print(geeks)
```

**Output:**

```py
[[64  1 12  3]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, -9]')

# applying matrix.ravel() method
geeks = gfg.ravel()

print(geeks)
```

**Output:**

```py
[[ 1  2  3  4  5  6  7  8 -9]]

```