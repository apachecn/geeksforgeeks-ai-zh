# Python 中的 numpy.pad()函数

> 原文:[https://www.geeksforgeeks.org/numpy-pad-function-in-python/](https://www.geeksforgeeks.org/numpy-pad-function-in-python/)

**numpy.pad()** 功能用于填充 numpy 数组。有时需要在 Numpy 数组中进行填充，则使用 **numPy.pad()** 功能。该函数返回与给定数组相等的填充数组，并且形状将根据 pad_width 增加。

> **语法:** numpy.pad(array，pad_width，mode='constant '，**kwargs)
> 
> **参数:**
> 
> *   **阵:**阵对垫
> *   **填充宽度:**此参数定义填充到每个轴边缘的值的数量。
>     **模式:**字符串或函数(可选)
> *   ****kwargs:** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> 
> **返回:**
> 秩等于数组的填充数组，形状根据 pad_width 增加。

**例 1:**

## 蟒蛇 3

```
# Python program to explain
# working of numpy.pad() function
import numpy as np

arr = [1, 3, 2, 5, 4]

# padding array using CONSTANT mode
pad_arr = np.pad(arr, (3, 2), 'constant', 
                 constant_values=(6, 4))

print(pad_arr)
```

**输出:**

```
[6 6 6 1 3 2 5 4 4 4]

```

**例 2:**

## 蟒蛇 3

```
# Python program to explain
# working of numpy.pad() function
import numpy as np

arr = [1, 3, 2, 5, 4] 

# padding array using 'linear_ramp' mode
pad_arr = np.pad(arr, (3, 2), 'linear_ramp',
                 end_values=(-4, 5))   

print(pad_arr)
```

**输出:**

```
[-4 -2 -1  1  3  2  5  4  4  5]

```

**例 3:**

## 蟒蛇 3

```
# Python program to explain
# working of numpy.pad() function
import numpy as np

arr = [1, 3, 9, 5, 4]

# padding array using 'maximum' mode
pad_arr = np.pad(arr, (3,), 'maximum')

print(pad_arr)
```

**输出:**

```
[9 9 9 1 3 9 5 4 9 9 9]

```

**例 4:**

## 蟒蛇 3

```
# Python program to explain
# working of numpy.pad() function
import numpy as np

arr = [[1, 3],[5, 8]] 

# padding array using 'minimum' mode
pad_arr = np.pad(arr, (3,), 'minimum')       

print(pad_arr)
```

**输出:**

```
[[1 1 1 1 3 1 1 1]
[1 1 1 1 3 1 1 1]
[1 1 1 1 3 1 1 1]
[1 1 1 1 3 1 1 1]
[5 5 5 5 8 5 5 5]
[1 1 1 1 3 1 1 1]
[1 1 1 1 3 1 1 1]
[1 1 1 1 3 1 1 1]]

```