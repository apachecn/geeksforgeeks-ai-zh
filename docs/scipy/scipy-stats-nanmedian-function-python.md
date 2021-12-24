# sciPy stats . nan middle()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-nan median-function-python/](https://www.geeksforgeeks.org/scipy-stats-nanmedian-function-python/)

`**scipy.stats.nanmedian(array, axis=0)**`函数通过忽略沿数组指定轴的数组元素的 Nan(不是数字)值来计算中位数。

> **参数:**
> **数组:**输入数组或对象所具有的元素，包括 Nan 值，来计算中位数。
> **轴:**计算中间值的轴。默认情况下，轴= 0
> 
> **根据设置的参数返回:**数组元素的中值(忽略 Nan 值)。

**代码#1:**

```py
# median 
import scipy
import numpy as np

arr1 = [1, 3, np.nan, 27, 2, 5] 

print("median using nanmedian :", scipy.nanmedian(arr1))

print("median without handling nan value :", scipy.median(arr1)) 
```

**输出:**

```py
median using nanmedian : 3.0
median without handling nan value : nan
```

**代码#2:** 有多维数据

```py
# median 
from scipy import median
from scipy import nanmedian
import numpy as np

arr1 = [[1, 3, 27], 
        [3, np.nan, 6], 
        [np.nan, 6, 3], 
        [3, 6, np.nan]] 

print("median is :", median(arr1)) 
print("median handling nan :", nanmedian(arr1)) 

# using axis = 0
print("\nmedian is with default axis = 0 : \n", 
      median(arr1, axis = 0))
print("\nmedian handling nan with default axis = 0 : \n", 
      nanmedian(arr1, axis = 0))

# using axis = 1
print("\nmedian is with default axis = 1 : \n", 
      median(arr1, axis = 1))  
print("\nmedian handling nan with default axis = 1 : \n", 
      nanmedian(arr1, axis = 1))  
```

**输出:**

```py
median is : nan
median handling nan : 3.0

median is with default axis = 0 : 
 [ nan  nan  nan]

median handling nan with default axis = 0 : 
 [ 3\.  6\.  6.]

median is with default axis = 1 : 
 [  3\.  nan  nan  nan]

median handling nan with default axis = 1 : 
 [ 3\.   4.5  4.5  4.5]
```