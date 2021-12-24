# Python | Numpy matrix . conj()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py-matrix-conj/

借助于`**Numpy matrix.conj()**`方法，我们能够找到具有一维或一维以上的给定矩阵的**共轭**。

> **语法:** `matrix.conj()`
> 
> **返回:** *返回给定矩阵的共轭*

**示例#1 :**
在这个示例中，我们可以看到`matrix.conj()`方法用于共轭矩阵。记住字符串类型的矩阵在这里不起作用。

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.matrix('[1 + 2j, 2 + 3j]')

# applying matrix.conj() method
geeks = gfg.conj()

print(geeks)
```

**Output:**

```py
[[ 1.-2.j  2.-3.j]]

```

**例 2 :**

```py
# import the important module in python
import numpy as np

# make an array with numpy
gfg = np.matrix('[1 + 2j, 2 + 3j, 3-2j; 1-4j, 2-3j, 7 + 8j]')

# applying matrix.conj() method
geeks = gfg.conj()

print(geeks)
```

**Output:**

```py
[[ 1.-2.j  2.-3.j  3.+2.j]
 [ 1.+4.j  2.+3.j  7.-8.j]]

```