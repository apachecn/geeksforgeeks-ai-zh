# Python 中的 numpy.clip()

> 原文:[https://www.geeksforgeeks.org/numpy-clip-in-python/](https://www.geeksforgeeks.org/numpy-clip-in-python/)

**`numpy.clip()`** 函数用于裁剪(限制)数组中的值。

给定一个区间，区间之外的值将被剪切到区间边缘。例如，如果指定的间隔为[0，1]，则小于 0 的值变为 0，大于 1 的值变为 1。

> **语法:** numpy.clip(a，a_min，a_max，out =无)
> 
> **参数:**
> **一:**阵含元素以夹。
> **a_min :** 最小值。
> –>如果无，则不在下间隔边缘进行剪裁。最小值和最大值中最多只能有一个为无。
> **a_max :** 最大值。
> –>如果无，不在上区间边缘进行裁剪。最小值和最大值中最多只能有一个为无。
> –>如果 a_min 或 a_max 是 array_like，那么这三个数组将被广播以匹配它们的形状。
> **出:**结果会放在这个数组中。它可能是就地剪辑的输入数组。out 的形状必须正确，才能容纳输出。它的类型得以保留。
> 
> **返回:**剪裁 _ 数组

**代码#1 :**

```
# Python3 code demonstrate clip() function

# importing the numpy
import numpy as np

in_array = [1, 2, 3, 4, 5, 6, 7, 8 ]
print ("Input array : ", in_array)

out_array = np.clip(in_array, a_min = 2, a_max = 6)
print ("Output array : ", out_array)
```

**输出:**

```
Input array :  [1, 2, 3, 4, 5, 6, 7, 8]
Output array :  [2 2 3 4 5 6 6 6]
```

**代码#2 :**

```
# Python3 code demonstrate clip() function

# importing the numpy
import numpy as np

in_array = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
print ("Input array : ", in_array)

out_array = np.clip(in_array, a_min =[3, 4, 1, 1, 1, 4, 4, 4, 4, 4],
                                                         a_max = 9)
print ("Output array : ", out_array)
```

**输出:**

```
Input array :  [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
Output array :  [3 4 3 4 5 6 7 8 9 9]

```