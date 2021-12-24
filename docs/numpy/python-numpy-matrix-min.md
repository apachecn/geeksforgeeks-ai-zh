# Python | Numpy matrix.min()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-matrix-min/

借助`**Numpy matrix.min()**`方法，我们可以从给定的矩阵中得到**的最小值**。

> **语法:** `matrix.min()`
> 
> **返回:** *从给定矩阵返回最小值*

**示例#1 :**
在这个示例中，我们可以看到，借助方法`matrix.min()`，我们能够从给定的矩阵中获得最小值。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1; 12, 3]')

# applying matrix.min() method
geeks = gfg.min()

print(geeks)
```

**Output:**

```py
1

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, -9]')

# applying matrix.min() method
geeks = gfg.min()

print(geeks)
```

**Output:**

```py
-9

```