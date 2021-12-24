# python | num py matrix . geti()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py 矩阵 geti/

借助`**Numpy matrix.getI()**`方法，我们可以得到与给定矩阵相同大小的**乘法逆**。

> **语法:** `matrix.getI()`
> 
> **返回:** *返回给定矩阵的乘法逆*

**例#1 :**
在这个例子中我们可以看到，我们能够借助方法`matrix.getI()`得到乘法逆。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[6, 1; 2, 3]')

# applying matrix.getI() method
geeks = gfg.getI()

print(geeks)
```

**Output:**

```
[[ 0.1875 -0.0625]
 [-0.125   0.375 ]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.getI() method
geeks = gfg.getI()

print(geeks)
```

**Output:**

```
[[ -4.50359963e+15   9.00719925e+15  -4.50359963e+15]
 [  9.00719925e+15  -1.80143985e+16   9.00719925e+15]
 [ -4.50359963e+15   9.00719925e+15  -4.50359963e+15]]

```