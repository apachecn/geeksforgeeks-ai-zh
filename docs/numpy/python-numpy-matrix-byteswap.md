# python | num py matrix . byteswap()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py 矩阵字节交换/

借助`**Numpy matrix.byteswap()**`方法，我们可以在给定的一维或多维矩阵中交换元素的字节位置。它不适用于字符串或字符类型的矩阵。

> **语法:** `matrix.byteswap()`
> 
> **返回:** *返回字节数组*

**示例#1 :**
在这个示例中，我们可以看到，借助`matrix.byteswap()`方法，我们能够交换给定矩阵中元素的字节位置。

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3, 4]')

# applying matrix.byteswap() method
geeks = gfg.byteswap()

print(geeks)
```

**Output:**

```
[[ 72057594037927936 144115188075855872 216172782113783808
  288230376151711744]]

```

**例 2 :**

```
# import the important module in python
import numpy as np

# make a matrix with numpy
gfg = np.matrix('[1, 2, 3; 4, 5, 6; 7, 8, 9]')

# applying matrix.byteswap() method
geeks = gfg.byteswap()

print(geeks)
```

**Output:**

```
[[ 72057594037927936 144115188075855872 216172782113783808]
 [288230376151711744 360287970189639680 432345564227567616]
 [504403158265495552 576460752303423488 648518346341351424]]

```