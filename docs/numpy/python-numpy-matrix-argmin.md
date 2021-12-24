# python | num py matrix . argmin()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-matrix-argmin/

借助于`**Numpy matrix.argmax()**`方法，我们能够在具有一维或多维的给定矩阵中找到**最小**元素的索引值。

> **语法:** `matrix.argmin()`
> 
> **返回:** *返回矩阵中最小元素的指标数*

**示例#1 :**
在这个示例中，我们可以看到借助于`matrix.argmax()`方法，我们能够找到给定矩阵中最小元素的索引。

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3, 4]')

# applying matrix.argmin() method
geeks = gfg.argmin()

print(geeks)
```

**Output:**

```py
0

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, -5, 6; 7, 8, 9]')

# applying matrix.argmin() method
geeks = gfg.argmin()

print(geeks)
```

**Output:**

```py
4

```