# 如何用 NumPy 计算两个给定向量的叉积？

> 原文:[https://www . geeksforgeeks . org/如何使用-numpy/](https://www.geeksforgeeks.org/how-to-compute-the-cross-product-of-two-given-vectors-using-numpy/) 计算两个给定向量的叉积

让我们看看用 NumPy 计算两个给定向量的叉积的程序。为了求两个给定向量的叉积，我们使用了 numpy 库的 **numpy.cross()** 函数。

> **语法:** numpy.cross( *a* 、 *b* 、 *axisa=-1* 、 *axisb=-1* 、 *axisc=-1* 、*axis = None*)[【](https://github.com/numpy/numpy/blob/v1.19.0/numpy/core/numeric.py#L1452-L1647)
> 
> **返回:**两个(数组)向量的叉积。

让我们看看例子:

**例 1:** 一维数组的叉积。

## 蟒蛇 3

```py
# import library
import numpy as np

# declare vectors
x = [1, 2]
y = [3, 4]

# find cross product of
# two given vectors
result = np.cross(x, y)

# show the result
print(result)
```

**输出:**

```py
-2

```

**例 2:** 二维数组的叉积。

## 蟒蛇 3

```py
# import library
import numpy as np

# declare vectors
x = [[1, 2], [3, 4]]
y = [[5, 6], [7, 8]]

# find cross product of
# two given vectors
result = np.cross(x, y)

# show the result
print(result)
```

**输出:**

```py
[-4 -4]

```