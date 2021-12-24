# Python | Numpy matrix . compress()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-compress/](https://www.geeksforgeeks.org/python-numpy-matrix-compress/)

借助`**Numpy matrix.compress()**`方法，我们可以通过将参数作为数组传递来选择矩阵中的元素，该数组包含值 0 以不包含元素，或者包含值 1 以包含矩阵中的元素。简单地说，我们在`matrix.compress()`方法中传递布尔数组。

> **语法:** `matrix.compress()`
> 
> **返回:** *返回压缩数组*

**示例#1 :**
在这个示例中，我们可以看到借助于`matrix.compress()`方法，我们能够压缩矩阵。

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3, 4; 3, 1, 5, 6]')

# applying matrix.compress() method
geeks = np.compress([1, 0, 1, 0, 1, 1], gfg)

print(geeks)
```

**Output:**

```py
[[1 3 3 1]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.compress() method
geeks = np.compress([1, 0, 1, 1, 1, 0, 0, 1, 1], gfg)

print(geeks)
```

**Output:**

```py
[[1 3 4 5 8 9]]

```