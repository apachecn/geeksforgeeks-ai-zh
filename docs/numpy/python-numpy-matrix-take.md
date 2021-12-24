# Python | Numpy matrix . take()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-take/](https://www.geeksforgeeks.org/python-numpy-matrix-take/)

借助`**Numpy matrix.take()**`方法，我们可以通过传递参数作为元素的索引值，从给定的矩阵中选择元素。它将返回一个一维矩阵。记住，它一次只对一个轴起作用。

> **语法:** `matrix.take(index, axis)`
> **返回:** **返回所选指标矩阵**

**示例#1 :**
在这个示例中，我们可以看到，通过使用`matrix.take()`方法选择一个索引，我们在矩阵中只能获得一个值。

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 12, 3, 4, 6, 7]')

# applying matrix.take() method
geek = gfg.take(2)

print(geek)
```

**Output:**

```py
[[12]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.take() method
geek = gfg.take(0, 1)

print(geek)
```

**Output:**

```py
[[ 4 12  4]]

```