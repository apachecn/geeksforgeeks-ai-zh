# sciPy stats . nantd()函数| Python

> 原文:[https://www . geesforgeks . org/scipy-stats-nantd-function-python/](https://www.geeksforgeeks.org/scipy-stats-nanstd-function-python/)

`**scipy.stats.nanstd(array, axis=0)**`函数通过忽略沿数组指定轴的数组元素的 Nan(不是数字)值来计算标准差。

是公式–
![](img/4a0d323535121aea9e67d9d58ee5e4f7.png)

> **参数:**
> **数组:**输入数组或对象所具有的元素，包括 Nan 值，来计算标准差。
> **轴:**计算标准偏差的轴。默认情况下，轴= 0
> 
> **根据设定的参数返回:**数组元素的标准差(忽略 Nan 值)。

**代码#1:**

```
# standard deviation 
import scipy
import numpy as np

arr1 = [1, 3, np.nan, 27] 

print("standard deviation using nanstd :", scipy.nanstd(arr1))

print("standard deviation without handling nan value :", scipy.std(arr1)) 
```

**输出:**

```
standard deviation using nanstd : 11.813363431112899
standard deviation without handling nan value : nan
```

**代码#2:** 多维数据

```
# standard deviation 
from scipy import std
from scipy import nanstd
import numpy as np

arr1 = [[1, 3, 27], 
        [3, np.nan, 6], 
        [np.nan, 6, 3], 
        [3, 6, np.nan]] 

print("standard deviation is :", std(arr1)) 
print("standard deviation handling nan :", nanstd(arr1)) 

# using axis = 0
print("\nstandard deviation is with default axis = 0 : \n", 
      std(arr1, axis = 0))
print("\nstandard deviation handling nan with default axis = 0 : \n", 
      nanstd(arr1, axis = 0))

# using axis = 1
print("\nstandard deviation is with default axis = 1 : \n", 
      std(arr1, axis = 1))  
print("\nstandard deviation handling nan with default axis = 1 : \n", 
      nanstd(arr1, axis = 1))  
```

**输出:**

```
standard deviation is : nan
standard deviation handling nan : 7.455216087651669

standard deviation is with default axis =0 : 
 [nan nan nan]

standard deviation handling nan with default axis =0 : 
 [ 0.94280904  1.41421356 10.67707825]

standard deviation is with default axis =1 : 
 [11.81336343         nan         nan         nan]

standard deviation handling nan with default axis =1 : 
 [11.81336343  1.5         1.5         1.5       ]
```