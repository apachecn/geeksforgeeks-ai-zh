# 加入 NumPy 阵列

> 原文:[https://www.geeksforgeeks.org/joining-numpy-array/](https://www.geeksforgeeks.org/joining-numpy-array/)

[NumPy](https://www.geeksforgeeks.org/python-numpy/) 提供各种功能组合数组。在本文中，我们将讨论一些主要的问题。

*   [numpy。串连〔t1〕](https://www.geeksforgeeks.org/numpy-concatenate-function-python/)
*   [numpy。堆栈〔t1〕](https://www.geeksforgeeks.org/numpy-stack-in-python/)
*   numpy(数码相机)。布洛克！布洛克

**方法 1:使用**[**numpy . concatenate()**](https://www.geeksforgeeks.org/numpy-concatenate-function-python/)

NumPy 中的 concatenate 函数沿着指定的轴连接两个或多个数组。

**语法:**

```py
numpy.concatenate((array1, array2, ...), axis=0)

```

第一个参数是我们打算连接的数组元组，第二个参数是我们需要连接这些数组的轴。下面的例子展示了使用 numpy . concatenate .

## python 3

```py
import numpy as np

array_1 = np.array([1, 2])
array_2 = np.array([3, 4])

array_new = np.concatenate((array_1, array_2))
print(array_new)
```

**输出:**

```py
[1 2 4 5]

```

默认情况下，轴的值设置为 0。您可以通过在第二个参数中指定轴的值来更改它。下面的代码沿行连接两个数组。

## 蟒 3

```py
import numpy as np

array_1 = np.array([[1, 2], [3, 4]])
array_2 = np.array([[5, 6], [7, 8]])

array_new = np.concatenate((array_1, array_2), axis=1)
print(array_new)
```

**输出:**

```py
[[1 2 5 6]
 [3 4 7 8]]

```

**方法二:使用**[**numpy . stack()**](https://www.geeksforgeeks.org/numpy-stack-in-python/)

NumPy 的 stack()函数沿着一个新的轴连接两个或多个数组。

**语法:**

```py
numpy.stack(arrays, axis=0)

```

下面的代码演示了 numpy.stack()的用法。

## 蟒 3

```py
import numpy as np

array_1 = np.array([1, 2, 3, 4])
array_2 = np.array([5, 6, 7, 8])

array_new = np.stack((array_1, array_2), axis=1)
print(array_new)
```

**输出:**

```py
[[1 5]
 [2 6]
 [3 7]
 [4 8]]

```

阵列沿着新的轴连接。

**方法 3: numpy.block()**

numpy.block 用于从嵌套的列表块创建 nd 数组。

**语法:**

```py
numpy.block(arrays)

```

以下示例解释了 numpy.block()的工作原理。

## 蟒 3

```py
import numpy as np

block_1 = np.array([[1, 1], [1, 1]])
block_2 = np.array([[2, 2, 2], [2, 2, 2]])
block_3 = np.array([[3, 3], [3, 3], [3, 3]])
block_4 = np.array([[4, 4, 4], [4, 4, 4], [4, 4, 4]])

block_new = np.block([
    [block_1, block_2],
    [block_3, block_4]
])

print(block_new)
```

**输出:**

```py
[[1 1 2 2 2]
 [1 1 2 2 2]
 [3 3 4 4 4]
 [3 3 4 4 4]
 [3 3 4 4 4]]

```

在本例中，我们从 4 个独立的二维数组(block_1、block_2、block_3、block_4)中组装了一个块矩阵(block_new)。