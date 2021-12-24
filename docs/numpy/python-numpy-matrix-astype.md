# python | num py matrix . asttype()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-astype/](https://www.geeksforgeeks.org/python-numpy-matrix-astype/)

借助`**Numpy matrix.astype()**`方法，我们能够转换矩阵的类型，但问题是数据丢失如果我们想将 float 转换为 int，那么一些数据将丢失。此方法有助于矩阵的**类型转换**。

> **语法:** `matrix.astype()`
> 
> **返回:** *类型转换后返回矩阵。*

**示例#1 :**
在这个示例中，我们可以看到如何使用`matrix.astype()`方法将浮点型矩阵转换为 int 型矩阵。

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1.2, 2.8, 3.1, 4.5]')

# applying matrix.astype() method
geeks = gfg.astype(int)

print(geeks)
```

**Output:**

```py
[[1 2 3 4]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1.1, 2, 3.5; 4.2, 5.5, 6; 7, 8, 9.3]')

# applying matrix.astype() method
geeks = gfg.astype(int)

print(geeks)
```

**Output:**

```py
[[1 2 3]
 [4 5 6]
 [7 8 9]]

```