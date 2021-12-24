# python | num py matrix . swap axes()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-swapaxes/](https://www.geeksforgeeks.org/python-numpy-matrix-swapaxes/)

借助`**matrix.swapaxes()**`方法，我们可以用同样的方法交换矩阵的轴。

> **语法:** `matrix.swapaxes()`
> **返回:**返回有互换轴的矩阵

**示例#1 :**
在本例中，我们可以使用`matrix.swapaxes()`方法交换矩阵的轴。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1; 12, 3]')

# applying matrix.swapaxes() method
geek = gfg.swapaxes(0, 1)

print(geek)
```

**Output:**

```
[[ 4 12]
 [ 1  3]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.swapaxes() method
geek = gfg.swapaxes(1, 1)

print(geek)
```

**Output:**

```
[[ 4  1  9]
 [12  3  1]
 [ 4  5  6]]

```