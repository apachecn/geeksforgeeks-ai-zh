# Python | Numpy matrix . resize()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-resize/](https://www.geeksforgeeks.org/python-numpy-matrix-resize/)

借助`**Numpy matrix.resize()**`方法，我们能够**调整**给定矩阵的形状。请记住，在调整给定矩阵的大小时，所有元素都应该被覆盖。

> **语法:** `matrix.resize(shape)`
> 
> **返回:** *新调整大小的矩阵*

**示例#1 :**
在给定示例中，我们可以使用`matrix.resize()`方法调整给定矩阵的大小。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[64, 1; 12, 3]')

# applying matrix.resize() method
geeks = gfg.resize((1, 4))

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
gfg = np.matrix('[1, 2; 4, 5; 7, 8]')

# applying matrix.resize() method
geeks = gfg.resize((2, 3))

print(geeks)
```

**Output:**

```py
[[1 2 4]
 [5 7 8]]

```