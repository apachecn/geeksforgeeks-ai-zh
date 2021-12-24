# Python Scipy–ndi image . map _ 坐标()函数

> 原文:[https://www . geesforgeks . org/python-scipy-ndi image-map _ coordinates-function/](https://www.geeksforgeeks.org/python-scipy-ndimage-map_coordinates-function/)

该函数用于通过插值将给定数组映射到新坐标。坐标数组用于为输出中的每个点查找输入中相应的坐标。

> **语法:**scipy . ndimage . map _ coordinates(输入，坐标，输出=无，顺序=3，cval=0.0，前置滤波器=真)
> 
> **参数**
> 
> *   输入:类似数组–输入数组。
> *   坐标:类似数组的坐标-计算输入的坐标。
> *   输出:它是一个数组–放置输出的数组。
> *   顺序:整数，可选，样条插值的顺序，
> *   cval:它是一个标量，-它是可选的，如果模式为“常量”，则填充输入边缘的值。默认值为 0.0。
> *   前置过滤器:它是布尔类型的，是可选的。它用于确定在插值之前输入数组是否经过了 spline_filter 的预滤波。
> 
> **返回:**地图坐标:ndarray

**例 1:**

## 蟒蛇 3

```
# importing numpy package for
# creating arrays
import numpy as np

# importing scipy
from scipy import ndimage

# creating an array from 0 to 15 values
a = np.arrange(16.).reshape((4, 4))

# finding coordinates
ndimage.map_coordinates(a, [[0.3, 1], [0.5, 1]], order=1)
```

**输出:**

```
array([1.7, 5\. ])
```

**例 2:**

## 蟒蛇 3

```
# importing numpy package for
# creating arrays
import numpy as np

# importing scipy
from scipy import ndimage

a = np.arrange(25.).reshape((5, 5))

vals = [[0.3, 1], [0.5, 1]]

# calculating mode
print(ndimage.map_coordinates(a, vals, order=1, mode='nearest'))
print(ndimage.map_coordinates(a, vals, order=1, cval=0, output=bool))
print(ndimage.map_coordinates(a, vals, order=1))
```

**输出:**

```
[2\. 6.]
[ True  True]
[2\. 6.]
```