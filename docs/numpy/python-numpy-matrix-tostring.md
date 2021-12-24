# python | num py matrix . tostring()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/python-num py 矩阵 tostring/

借助`**Numpy matrix.tostring()**`方法，我们可以使用`matrix.tostring()`方法为矩阵找到字符串格式的字节码。

> **语法:** `matrix.tostring()`
> **返回:** **返回矩阵的字节码串**

**示例#1 :**
在这个示例中，我们可以看到，通过使用`**matrix.tostring()**`方法，我们能够找到给定矩阵的字符串格式的字节代码。

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1; 12, 3]')

# applying matrix.tostring() method
geek = gfg.tostring()

print(geek)
```

**Output:**

> b ' \ x04 \ x00 \ x00 \ x00 \ x00 \ x00 \ x01 \ x00 \ x00 \ x00 \ x00 \ x00 \ x00 \ x0c \ x00 \ x00 \ x00 \ x00 \ x00 \ x03 \ x00 \ x00 \ x00 \ x00 \ x00 \ x00′

**例 2 :**

```
# import the important module in python
import numpy as np

# make matrix with numpy
gfg = np.matrix('[4, 1, 9; 12, 3, 1; 4, 5, 6]')

# applying matrix.tostring() method
geek = gfg.tostring()

print(geek)
```

**Output:**

> b ' \ p04 \ x000 \ x000 \ x000 \ x000 \ x000 \ x000 \ x000 \ x000 \ x000 \ 0x 00 \ 0x 00 \ t0c \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 01 \ x 01 \ n