# python | num py . matrix . all()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-num py-matrix-all/

借助`**Numpy numpy.matrix.all()**`方法，我们能够将一个矩阵的每个元素与另一个进行比较，或者我们可以提供我们想要应用比较的轴。

> **语法:** `numpy.matrix.all()`
> 
> **返回:** *如果发现匹配则返回真否则返回假*

**例#1 :**
在这个例子中我们可以看到，借助`matrix.all()`方法，我们能够比较任意两个维度不同的矩阵。

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg1 = np.matrix('[1, 2, 3, 4]')
gfg2 = np.matrix('[1, 2, 3, 4]')

# applying matrix.all() method
geeks = (gfg1 == gfg2).all()

print(geeks)
```

**Output:**

```
True

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg1 = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')
gfg2 = np.matrix('[1, 2, 3]')

# applying matrix.all() method
geeks = (gfg1 == gfg2).all()

print(geeks)
```

**Output:**

```
False

```