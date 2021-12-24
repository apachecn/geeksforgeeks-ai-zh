# Python 中的 numpy.around()

> 原文:[https://www.geeksforgeeks.org/numpy-around-python/](https://www.geeksforgeeks.org/numpy-around-python/)

**numpy . round(arr，decimals = 0，out = None) :** 这个数学函数帮助用户将数组元素均匀地舍入到给定的小数位数。

**参数:**

> **阵:** *【阵 _ 象】*输入阵。
> **小数:***【int，可选】*我们要四舍五入的小数位数。
> 
> 默认值= 0。如果是-ve 小数，它指定 n0。小数点左边的位置。
> 
> **出:** *【可选】*输出结果阵

**返回:**

```py
An array with all array elements being rounded off,
having same type as input 
```

**代码#1:工作**

```py
# Python program explaining
# around() function

import numpy as np

in_array = [.5, 1.5, 2.5, 3.5, 4.5, 10.1]
print ("Input array : \n", in_array)

round_off_values = np.around(in_array)
print ("\nRounded values : \n", round_off_values)

in_array = [.53, 1.54, .71]
print ("\nInput array : \n", in_array)

round_off_values = np.around(in_array)
print ("\nRounded values : \n", round_off_values)

in_array = [.5538, 1.33354, .71445]
print ("\nInput array : \n", in_array)

round_off_values = np.around(in_array, decimals = 3)
print ("\nRounded values : \n", round_off_values)
```

**输出:**

```py
Input array : 
 [0.5, 1.5, 2.5, 3.5, 4.5, 10.1]

Rounded values : 
 [  0\.   2\.   2\.   4\.   4\.  10.]

Input array : 
 [0.53, 1.54, 0.71]

Rounded values : 
 [ 1\.  2\.  1.]

Input array : 
 [0.5538, 1.33354, 0.71445]

Rounded values : 
 [ 0.554  1.334  0.714]
```

**代码 2:工作**

```py
# Python program explaining
# around() function

import numpy as np

in_array = [1 ,4, 7, 9, 12]
print ("Input array : \n", in_array)

round_off_values = np.around(in_array)
print ("\nRounded values : \n", round_off_values)

in_array = [133 ,344, 437, 449, 12]
print ("\nInput array : \n", in_array)

round_off_values = np.around(in_array, decimals = -2)
print ("\nRounded values upto 2: \n", round_off_values)

in_array = [133 ,344, 437, 449, 12]
print ("\nInput array : \n", in_array)

round_off_values = np.around(in_array, decimals = -3)
print ("\nRounded values upto 3: \n", round_off_values)
```

**输出:**

```py
Input array : 
 [1, 4, 7, 9, 12]

Rounded values : 
 [ 1  4  7  9 12]

Input array : 
 [133, 344, 437, 449, 12]

Rounded values upto 2: 
 [100 300 400 400   0]

Input array : 
 [133, 344, 437, 449, 12]

Rounded values upto 3: 
 [0 0 0 0 0]

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . about . html # numpy . about](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.around.html#numpy.around)
。