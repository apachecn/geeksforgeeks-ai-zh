# python | num py matrix . argsort()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-matrix-argsort/

借助`**Numpy matrix.argmax()**`方法，我们能够找到**排序**给定矩阵中具有一个或多个维度的元素，并且它将返回排序元素的索引值。

> **语法:** `matrix.argsort()`
> 
> **返回:** *返回矩阵中排序元素的索引号*

**示例#1 :**
在这个示例中我们可以看到，借助`matrix.argsort()`方法，我们能够在给定的矩阵中找到排序的元素，并给出作为排序数组索引的输出。

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, -2, 3, -4]')

# applying matrix.argsort() method
geeks = gfg.argsort()

print(geeks)
```

**Output:**

```
[[3 1 0 2]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[-1, 2, 3; 4, -5, 6; 7, -8, 9]')

# applying matrix.argsort() method
geeks = gfg.argsort()

print(geeks)
```

**Output:**

```
[[0 1 2]
 [1 0 2]
 [1 0 2]]

```