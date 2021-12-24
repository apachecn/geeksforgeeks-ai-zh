# Python | Numpy matrix . fill()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-fill/](https://www.geeksforgeeks.org/python-numpy-matrix-fill/)

借助`**Numpy matrix.fill()**`方法，我们能够在给定的矩阵中填充一个`scalar value`，并以具有标量值的矩阵给出输出。

> **语法:** `matrix.fill(value)`
> 
> **返回:** *返回一个有标量值的矩阵*

**示例#1 :**
在这个示例中，我们可以看到借助于`matrix.fill()`方法，我们能够用标量值填充给定的矩阵。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6, 2, 3]')

# applying matrix.fill() method
gfg.fill(0)

print(gfg)
```

**Output:**

```py
[[0 0 0]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6]')

# applying matrix.fill() method
gfg.fill(1)

print(gfg)
```

**Output:**

```py
[[1 1 1]
 [1 1 1]]

```