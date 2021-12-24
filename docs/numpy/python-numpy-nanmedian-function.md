# Python | Numpy nan middle()函数

> 原文:[https://www . geeksforgeeks . org/python-numpy-nan median-function/](https://www.geeksforgeeks.org/python-numpy-nanmedian-function/)

**numpy . NaN middle()**函数可以用来计算忽略 NaN 值的数组的中值。如果数组有 NaN 值，我们可以在不影响 NaN 值的情况下求出中值。让我们看看关于 numpy.nanmedian()方法的不同类型的例子。

> **语法:**numpy . nan middle(a，axis=None，out=None，overwrite_input=False，keepdims=)
> **参数:**
> **a:**【arr _ like】输入数组
> **axis:** 我们可以用 axis=1 表示行方向，axis=0 表示列方向。
> **出:**输出数组
> **overwrite_input:** 如果为真，则允许使用输入数组 a 的内存进行计算。对中值的调用将修改输入数组。
> **保持尺寸:**如果设置为真，减少的轴将作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将正确地广播到原始 a.
> **返回:**返回 n 数组中的中间值。

**示例#1:**

## 蟒蛇 3

```
# Python code to demonstrate the
# use of numpy.nanmedian
import numpy as np

# create 2d array with nan value.
arr = np.array([[12, 10, 34], [45, 23, np.nan]])

print("Shape of array is", arr.shape)

print("Median of array without using nanmedian function:",
                                           np.median(arr))

print("Using nanmedian function:", np.nanmedian(arr))
```

**输出:**

```
Shape of array is (2, 3)
Median of array without using nanmedian function: nan
Using nanmedian function: 23.0
```

**例 2:**

## 蟒蛇 3

```
# Python code to demonstrate the
# use of numpy.nanmedian
# with axis
import numpy as np

# create 2d array with nan value.
arr = np.array([[12, 10, 34], [45, 23, np.nan]])

print("Shape of array is", arr.shape)

print("Median of array with axis = 0:",
             np.median(arr, axis = 0))

print("Using nanmedian function:",
      np.nanmedian(arr, axis = 0))
```

**输出:**

```
Shape of array is (2, 3)
Median of array with axis = 0: [ 28.5  16.5   nan]
Using nanmedian function: [ 28.5  16.5  34\. ]
```

**示例#3:**

## 蟒蛇 3

```
# Python code to demonstrate the
# use of numpy.nanmedian
# with axis = 1
import numpy as np

# create 2d matrix with nan value
arr = np.array([[12, 10, 34],
                [45, 23, np.nan], 
                [7, 8, np.nan]])

print("Shape of array is", arr.shape)

print("Median of array with axis = 0:",
             np.median(arr, axis = 1))

print("Using nanmedian function:",
      np.nanmedian(arr, axis = 1))
```

**输出:**

```
Shape of array is (3, 3)
Median of array with axis = 0: [ 12\.  nan  nan]
Using nanmedian function: [ 12\.   34\.    7.5]
```