# python \ numpy matrix . gett()

> 原文:[https://www.geeksforgeeks.org/python-numpy-matrix-gett/](https://www.geeksforgeeks.org/python-numpy-matrix-gett/)

借助`**Numpy matrix.getT()**`方法，我们可以得到与给定矩阵相同大小的**转置**。

> **语法:** `matrix.getT()`
> 
> **返回:** *返回给定矩阵的转置*

**例 1 :**
在这个例子中我们可以看到，借助方法`matrix.getT()`，我们能够得到**转置**。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6, 1; 2, 3]')

# applying matrix.getT() method
geeks = gfg.getT()

print(geeks)
```

**Output:**

```
[[6 2]
 [1 3]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.getT() method
geeks = gfg.getT()

print(geeks)
```

**Output:**

```
[[1 4 7]
 [2 5 8]
 [3 6 9]]

```