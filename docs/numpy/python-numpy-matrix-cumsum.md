# python | num py matrix . cum sum()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-matrix-cum sum/

借助`**Numpy matrix.cumsum()**`方法，我们能够找到给定矩阵的`cumulative sum`，并以一维矩阵的形式给出输出。

> **语法:** `matrix.cumsum()`
> 
> **返回:** *返回矩阵累计和*

**示例#1 :**
在这个示例中，我们可以看到，借助`matrix.cumsum()`方法，我们能够找到给定数组的累积和。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6, 2, 3]')

# applying matrix.cumsum() method
geeks = gfg.cumsum()

print(geeks)
```

**Output:**

```
[[ 6  8 11]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6]')

# applying matrix.cumsum() method
geeks = gfg.cumsum()

print(geeks)
```

**Output:**

```
[[ 1  3  6 10 15 21]]

```