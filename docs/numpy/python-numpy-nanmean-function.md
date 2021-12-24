# Python | numpy.nanmean()函数

> 原文:[https://www . geesforgeks . org/python-numpy-nan mean-function/](https://www.geeksforgeeks.org/python-numpy-nanmean-function/)

**numpy.nanmean()** 函数可以用来计算忽略 NaN 值的数组的平均值。如果数组中有 NaN 值，我们可以在不影响 NaN 值的情况下求出平均值。

> **语法:** numpy.nanmean(a，axis=None，dtype=None，out=None，keepdims =)
> **参数:**
> **a:**【arr _ like】输入数组
> **axis:** 我们可以用 axis=1 表示行方向或者 axis=0 表示列方向。
> **出:**输出数组
> **数据类型:**数组的数据类型
> **overwrite_input:** 如果为真，则允许使用输入数组 a 的内存进行计算。对中值的调用将修改输入数组。
> **保持尺寸:**如果设置为真，缩小的轴将作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将会正确地广播到原始 a 中。
> **返回:**返回数组元素的平均值

**示例#1:**

## 蟒蛇 3

```py
# Python code to demonstrate the
# use of numpy.nanmean
import numpy as np

# create 2d array with nan value.
arr = np.array([[20, 15, 37], [47, 13, np.nan]])

print("Shape of array is", arr.shape)

print("Mean of array without using nanmean function:",
                                           np.mean(arr))

print("Using nanmean function:", np.nanmean(arr))
```

**Output:** 

```py
Shape of array is (2, 3)
Mean of array without using nanmean function: nan
Using nanmean function: 26.4
```

**例 2:**

## 蟒蛇 3

```py
# Python code to demonstrate the
# use of numpy.nanmean
# with axis = 0
import numpy as np

# create 2d matrix with nan value
arr = np.array([[32, 20, 24],
                [47, 63, np.nan],  
                [17, 28, np.nan],
                [10, 8, 9]])

print("Shape of array is", arr.shape)

print("Mean of array with axis = 0:",
             np.mean(arr, axis = 0))

print("Using nanmedian function:",
      np.nanmean(arr, axis = 0))
```

**Output:** 

```py
Shape of array is (4, 3)
Mean of array with axis = 0: [ 26.5   29.75    nan]
Using nanmedian function: [ 26.5   29.75  16.5 ]
```

**例 3:**

## 蟒蛇 3

```py
# Python code to demonstrate the
# use of numpy.nanmedian
# with axis = 1
import numpy as np

# create 2d matrix with nan value
arr = np.array([[32, 20, 24],
                [47, 63, np.nan],  
                [17, 28, np.nan],
                [10, 8, 9]])

print("Shape of array is", arr.shape)

print("Mean of array with axis = 1:",
             np.mean(arr, axis = 1))

print("Using nanmedian function:",
      np.nanmean(arr, axis = 1))
```

**Output:** 

```py
Shape of array is (4, 3)
Mean of array with axis = 1: [ 25.33333333          nan          nan   9\.        ]
Using nanmedian function: [ 25.33333333  55\.          22.5          9\.        ]
```