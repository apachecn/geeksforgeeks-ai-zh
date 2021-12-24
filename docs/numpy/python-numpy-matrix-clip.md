# Python | Numpy matrix . clip()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-clip/](https://www.geeksforgeeks.org/python-numpy-matrix-clip/)

借助`**Numpy matrix.clip()**`方法，我们可以通过传递一个参数作为**最小**值和**最大**值来从矩阵中选择元素。在这些参数和矩阵大小之间有一个范围的输出数组是相同的。

> **语法:** `matrix.clip()`
> 
> **返回:** *返回一个值介于最小值和最大值之间的矩阵。*

**示例#1 :**
在这个示例中，我们可以看到借助于`matrix.clip()`方法，我们能够将矩阵夹在最小值和最大值之间。

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3, 4; 3, 1, 5, 6]')

# applying matrix.clip() method
geeks = gfg.clip(1, 4)

print(geeks)
```

**Output:**

```py
[[1 2 3 4]
 [3 1 4 4]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.clip() method
geeks = gfg.clip(4, 9)

print(geeks)
```

**Output:**

```py
[[4 4 4]
 [4 5 6]
 [7 8 9]]

```