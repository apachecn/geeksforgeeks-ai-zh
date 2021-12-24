# 如何在 NumPy 中设置行和列的轴？

> 原文:[https://www . geeksforgeeks . org/如何为 numpy 中的行和列设置轴/](https://www.geeksforgeeks.org/how-to-set-axis-for-rows-and-columns-in-numpy/)

在本文中，我们将看到如何在 NumPy 中设置行和列的轴。

### 使用的功能

*   **np.array(对象):**要创建 NumPy 数组，对象是包含数组的参数
*   [**NP . resform(行、列):**](https://www.geeksforgeeks.org/numpy-reshape-python/) 将数组重塑为指定数量的行和列。在下面的例子中，我们用-1 代替行，让 numpy 算出每行是否有 3 列。
*   [**np.sum(轴):**](https://www.geeksforgeeks.org/numpy-sum-in-python/) 计算元素的和或加。在这里，我们已经提到了根据需求进行数组、行或列操作的轴。

**例 1:设置轴进行阵列式计算**

在本例中，我们将把 NumPy 数组重新整形为各有 3 列的行，即 nparray . resform(-1，3)，使其成为二维的。然后，我们将按正常顺序从 NumPy 数组的第一个到最后一个元素开始，按数组方式执行数组元素的求和操作。我们特别设置轴=无来触发正常的阵列式操作。

**代码:**

## 蟒蛇 3

```py
import numpy as np
nparray = np.array([[1, 2, 3], [11, 22, 33],
                    [4, 5, 6], [8, 9, 10], 
                    [20, 30, 40]])

nparray = nparray.reshape(-1, 3)
print(nparray)

# calculating sum along 
# axix=None i.e array-wise
output = nparray.sum(axis=None)
print("\n\nSum array-wise: ", output)
```

**输出:**

```py
[[ 1  2  3]
 [11 22 33]
 [ 4  5  6]
 [ 8  9 10]
 [20 30 40]]

Sum array-wise:  204
```

**例 2:设置轴进行列式计算**

在本例中，我们将把 numpy 数组重新整形为各有 3 列的行。然后使用 sum()函数逐列执行数组元素的求和操作。我们特别将轴设置为 0，以触发正常的阵列式操作。

**代码:**

## 蟒蛇 3

```py
import numpy as np

nparray = np.array([[1, 2, 3], [11, 22, 33],
                    [4, 5, 6], [8, 9, 10],
                    [20, 30, 40]])
nparray = nparray.reshape(-1, 3)
print(nparray)

# calculating sum along axix=0 
# i.e column-wise
output = nparray.sum(axis = 0)
print("\n\nSum column-wise: ", output)
```

**输出:**

```py
[[ 1  2  3]
 [11 22 33]
 [ 4  5  6]
 [ 8  9 10]
 [20 30 40]]

Sum column-wise:  [44 68 92]
```

**例 3:设置轴进行逐行计算**

我们将特别设置 axis = 1 来触发正常的逐行计算。

**代码:**

## 蟒蛇 3

```py
import numpy as np
nparray = np.array([[1, 2, 3], [11, 22, 33],
                    [4, 5, 6], [8, 9, 10], 
                    [20, 30, 40]])

nparray = nparray.reshape(-1, 3)
print(nparray)

# calculating sum along axix=1 
# i.e row0wise
output = nparray.sum(axis = 1)
print("\n\nSum row-wise: ", output)
```

**输出:**

```py
[[ 1  2  3]
 [11 22 33]
 [ 4  5  6]
 [ 8  9 10]
 [20 30 40]]

Sum row-wise:  [ 6 66 15 27 90]
```