# Python | Numpy matrix.dot()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-dot/](https://www.geeksforgeeks.org/python-numpy-matrix-dot/)

借助`**Numpy matrix.dot()**`方法，我们能够找到两个给定矩阵的`product`，并以新的维度矩阵给出输出。

> **语法:** `matrix.dot()`
> 
> **返回:** *返回两个矩阵的乘积*

**例#1 :**
在这个例子中我们可以看到借助`matrix.dot()`方法我们能够找到两个给定矩阵的乘积。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg1 = np.matrix('[6, 2, 3]')
gfg2 = np.matrix('[4; 5; 9]')

# applying matrix.dot() method
geeks = gfg1.dot(gfg2)

print(geeks)
```

**Output:**

```
[[61]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg1 = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')
gfg2 = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.dot() method
geeks = gfg1.dot(gfg2)

print(geeks)
```

**Output:**

```
[[ 30  36  42]
 [ 66  81  96]
 [102 126 150]]

```