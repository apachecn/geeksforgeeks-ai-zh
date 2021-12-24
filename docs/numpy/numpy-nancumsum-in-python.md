# num py . nanum()在 Python

中

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-nanum-in-python/

**`numpy.nancumsum()`** 函数用于计算给定轴上数组元素的累积和，将非数字视为零。
遇到 nan，前导 nan 被零替换时，累计和不变。对于全为-NaN 或空的切片，将返回零。

> **语法:** numpy.nancumsum(arr，axis =无，dtype =无，out =无)
> 
> **参数:**
> **arr:**【Array _ like】包含需要累加和的数字的数组。如果 arr 不是数组，则尝试转换。
> **轴:**轴，沿着该轴计算累计总和。默认值是计算展平数组的总和。
> **数据类型:**返回数组的类型，以及元素相乘的累加器的类型。如果未指定 dtype，则默认为 arr 的 dtype，除非 arr 具有精度小于默认平台整数的整数 dtype。在这种情况下，将使用默认的平台整数。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **Return :** 除非指定 out，否则将返回一个保存结果的新数组，在这种情况下，将返回该数组。

**代码#1:工作**

```py
# Python program explaining
# numpy.nancumsum() function

import numpy as geek
in_num = 10

print ("Input  number : ", in_num)

out_sum = geek.nancumsum(in_num) 
print ("cumulative sum of input number : ", out_sum) 
```

**输出:**

```py
Input  number :  10
cumulative sum of input number :  [10]

```

**代码#2 :**

```py
# Python program explaining
# numpy.nancumsum() function

import numpy as geek

in_arr = geek.array([[2, 4, 6], [1, 3, geek.nan]])

print ("Input array : ", in_arr) 

out_sum = geek.nancumsum(in_arr) 
print ("cumulative sum of array elements: ", out_sum) 
```

**输出:**

```py
Input array :  [[  2\.   4\.   6.]
 [  1\.   3\.  nan]]
cumulative sum of array elements:  [  2\.   6\.  12\.  13\.  16\.  16.]

```

**代码#3 :**

```py
# Python program explaining
# numpy.nancumsum() function

import numpy as geek

in_arr = geek.array([[2, 4, 6], [1, 3, geek.nan]])

print ("Input array : ", in_arr) 

out_sum = geek.nancumsum(in_arr, axis = 0) 
print ("cumulative sum of array elements taking axis 0: ", out_sum) 
```

**输出:**

```py
Input array :  [[  2\.   4\.   6.]
 [  1\.   3\.  nan]]
cumulative sum of array elements taking axis 0:  [[ 2\.  4\.  6.]
 [ 3\.  7\.  6.]]

```