# Python | Numpy matrix . item()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-item/](https://www.geeksforgeeks.org/python-numpy-matrix-item/)

借助`**Numpy matrix.item()**`方法，我们只需提供索引号就可以从给定的矩阵中得到**项**，对于多维矩阵，我们可以通过给出索引值元组来得到该项。

> **语法:** `matrix.item(index)`
> 
> **返回:** *从给定矩阵返回物品*

**示例#1 :**
在这个示例中，我们可以看到，通过提供索引号，我们能够借助方法`matrix.item()`获得该物品。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6, 1; 2, 3]')

# applying matrix.item() method
geeks = gfg.item((1, 0))

print(geeks)
```

**Output:**

```
2

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.item() method
geeks = gfg.item((2, 0))

print(geeks)
```

**Output:**

```
7

```