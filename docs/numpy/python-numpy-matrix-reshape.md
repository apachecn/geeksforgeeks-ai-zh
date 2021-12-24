# Python | Numpy matrix . resform()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-reshape/](https://www.geeksforgeeks.org/python-numpy-matrix-reshape/)

借助`**Numpy matrix.reshape()**`方法，我们能够**重塑**给定矩阵的形状。请记住，在对给定矩阵进行整形后，所有元素都应该被覆盖。

> **语法:** `matrix.reshape(shape)`
> 
> **回归:** *新换阵*

**示例#1 :**
在给定的示例中，我们能够使用`matrix.reshape()`方法重塑给定的矩阵。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1; 12, 3]')

# applying matrix.reshape() method
geeks = gfg.reshape((1, 4))

print(geeks)
```

**Output:**

```
[[64  1 12  3]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2; 4, 5; 7, 8]')

# applying matrix.reshape() method
geeks = gfg.reshape((2, 3))

print(geeks)
```

**Output:**

```
[[1 2 4]
 [5 7 8]]

```