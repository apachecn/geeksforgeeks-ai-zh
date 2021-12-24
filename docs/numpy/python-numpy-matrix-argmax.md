# python | num py matrix . argmax()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-argmax/](https://www.geeksforgeeks.org/python-numpy-matrix-argmax/)

借助于`**Numpy matrix.argmax()**`方法，我们能够在具有一维或多维的给定矩阵中找到**最大**元素的索引值。

> **语法:** `matrix.argmax()`
> 
> **返回:** *返回矩阵中最大元素的索引号*

**例#1 :**
在这个例子中我们可以看到，借助`matrix.argmax()`方法，我们能够找到给定矩阵中最大元素的索引。

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3, 4]')

# applying matrix.argmax() method
geeks = gfg.argmax()

print(geeks)
```

**Output:**

```py
3

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.argmax() method
geeks = gfg.argmax()

print(geeks)
```

**Output:**

```py
8

```