# 计算两个给定 NumPy 阵列的皮尔逊积矩相关系数

> 原文:[https://www . geeksforgeeks . org/compute-Pearson-乘积-矩-相关系数-两个给定的 numpy-arrays/](https://www.geeksforgeeks.org/compute-pearson-product-moment-correlation-coefficients-of-two-given-numpy-arrays/)

在 NumPy 中，我们可以借助 **numpy.corrcoef()** 函数计算两个给定阵列的皮尔逊积矩相关系数。

在这个函数中，我们将数组作为参数传递，它将返回两个给定数组的皮尔逊积矩相关系数。

> **语法:** numpy.corrcoef(x，y=None，rowvar=True，bias=，ddof=)
> **返回:**皮尔逊积矩相关系数

让我们看一个例子:

**例 1:**

## 计算机编程语言

```
# import library
import numpy as np

# create numpy 1d-array
array1 = np.array([0, 1, 2])
array2 = np.array([3, 4, 5])

# pearson product-moment correlation
# coefficients of the arrays
rslt = np.corrcoef(array1, array2)

print(rslt)
```

**输出**

```
[[1\. 1.]
 [1\. 1.]]

```

**例 2:**

## 计算机编程语言

```
# import numpy library
import numpy as np

# create a numpy 1d-array
array1 = np.array([ 2, 4, 8])
array2 = np.array([ 3, 2,1])

# pearson product-moment correlation
# coefficients of the arrays
rslt2 = np.corrcoef(array1, array2)

print(rslt2)
```

**输出**

```
[[ 1\.         -0.98198051]
 [-0.98198051  1\.        ]]

```