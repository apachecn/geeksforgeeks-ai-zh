# Python | Numpy matrix . flat()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-flatten/](https://www.geeksforgeeks.org/python-numpy-matrix-flatten/)

借助`**Numpy matrix.flatten()**`方法，我们能够对给定的矩阵进行`flatten`，并给出一维矩阵的输出。

> **语法:** `matrix.flatten()`
> 
> **返回:** *返回展平一维矩阵*

**示例#1 :**
在这个示例中，我们可以看到借助`matrix.flatten()`方法，我们能够展平给定的矩阵。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6; 2; 3]')

# applying matrix.flatten() method
geeks = gfg.flatten()

print(geeks)
```

**Output:**

```
[[6 2 3]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.flatten() method
geeks = gfg.flatten()

print(geeks)
```

**Output:**

```
[[1 2 3 4 5 6 7 8 9]]

```