# Python | Numpy matrix . view()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-view/](https://www.geeksforgeeks.org/python-numpy-matrix-view/)

借助`**Numpy matrix.view()**`方法，我们可以用`matrix.view()`方法找到矩阵的新视图。

> **语法:** `matrix.view()`
> **返回:** **返回相同矩阵的新视图**

**示例#1 :**
在这个示例中，我们可以看到，通过使用`**matrix.view()**`方法，我们能够找到给定矩阵的新视图。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1; 12, 3]')

# applying matrix.view() method
geek = gfg.view()

print(geek)
```

**Output:**

```
[[ 4  1]
 [12  3]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.view() method
geek = gfg.view()

print(geek)
```

**Output:**

```
[[ 4  1  9]
 [12  3  1]
 [ 4  5  6]]

```