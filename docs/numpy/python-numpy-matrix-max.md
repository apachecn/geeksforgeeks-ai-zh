# Python | Numpy matrix.max()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-matrix-max/

借助`**Numpy matrix.max()**`方法，我们可以从给定的矩阵中得到**的最大**值。

> **语法:** `matrix.max()`
> 
> **返回:** *返回给定矩阵的最大值*

**示例#1 :**
在这个示例中，我们可以看到，借助方法`matrix.max()`，我们能够从给定的矩阵中获得最大值。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1; 12, 3]')

# applying matrix.max() method
geeks = gfg.max()

print(geeks)
```

**Output:**

```py
64

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.max() method
geeks = gfg.max()

print(geeks)
```

**Output:**

```py
9

```