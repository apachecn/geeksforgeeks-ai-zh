# Python 中的 numpy.nan_to_num()

> 原文:[https://www.geeksforgeeks.org/numpy-nan_to_num-in-python/](https://www.geeksforgeeks.org/numpy-nan_to_num-in-python/)

**`numpy.nan_to_num()`** 函数用于当我们想在一个数组中用零替换 nan(Not A Number)，用有限个数替换 inf。它返回具有非常大的数字的(正)无穷大和具有非常小的(负)数字的负无穷大。

> **语法:** numpy.nan_to_num(arr，copy=True)
> 
> **参数:**
> **arr :** 【阵样】输入数据。
> **复制:**【bool，可选】是创建 arr 的副本(True)还是就地替换值(False)。仅当转换到数组不需要拷贝时，就地操作才会发生。默认值为真。
> 
> **返回:**【ndarray】新数组，其形状与 arr 相同，并且 arr 中元素的数据类型具有最高精度。如果 arr 不精确，则 NaN 被零替换，infinity (-infinity)被适合输出数据类型的最大(最小或最负)浮点值替换。如果 arr 不是不精确的，则返回 arr 的副本。

**代码#1:工作**

```py
# Python program explaining
# numpy.nan_to_num() function

import numpy as geek
in_num = geek.nan

print ("Input  number : ", in_num)

out_num = geek.nan_to_num(in_num) 
print ("output  number : ", out_num) 
```

**输出:**

```py
Input  number :  nan
output  number :  0.0

```

**代码#2 :**

```py
# Python program explaining
# numpy.nan_to_num function

import numpy as geek

in_arr = geek.array([[2, geek.inf, 2], [2, 2, geek.nan]])

print ("Input array : ", in_arr) 

out_arr = geek.nan_to_num(in_arr) 
print ("output array: ", out_arr) 
```

**输出:**

```py
Input array :  [[  2\.  inf   2.]
 [  2\.   2\.  nan]]
output array:  [[  2.00000000e+000   1.79769313e+308   2.00000000e+000]
 [  2.00000000e+000   2.00000000e+000   0.00000000e+000]]

```

**代码#3 :**

```py
# Python program explaining
# numpy.nan_to_num function

import numpy as geek

in_arr = geek.array([[2, 2, 2], [2, 2, 6]])

print ("Input array : ", in_arr) 

out_arr = geek.nan_to_num(in_arr) 
print ("Output array: ", out_arr) 
```

**输出:**

```py
Input array :  Input array :  [[2 2 2]
 [2 2 6]]
Output array:  [[2 2 2]
 [2 2 6]]

```