# Python 中的 numpy.unpackbits()

> 原文:[https://www.geeksforgeeks.org/numpy-unpackbits-in-python/](https://www.geeksforgeeks.org/numpy-unpackbits-in-python/)

**`numpy.unpackbits()`** 是 numpy 中做二进制运算的另一个函数。它用于将 uint8 数组的元素解包为二进制值的输出数组。

> **语法:** numpy.unpackbits(arr，axis=None)
> 
> **参数:**
> **arr:**【array _ like ndarray】应该解包元素的 uint8 类型数组。
> **轴:**完成开箱的尺寸。如果没有，则在扁平数组中进行解包。
> 
> **返回:**【解包数组】uint8 类型的数组，其元素是二进制值(0 或 1)。

**代码#1 :**

```
# Python program explaining
# numpy.unpackbits() function

# importing numpy
import numpy as geek

# creating input array using 
# array function
in_arr = geek.array([171,  16], dtype = geek.uint8)
print ("Input array : ", in_arr) 

# unpacking elements of an array
# using unpackbits() function
out_arr = geek.unpackbits(in_arr)

print ("Output unpacked array : ", out_arr)
```

**Output :**

```
Input array :  [171  16]
Output unpacked array :  [1 0 1 0 1 0 1 1 0 0 0 1 0 0 0 0]

```

**代码#2 :**

```
# Python program explaining
# numpy.unpackbits() function

# importing numpy
import numpy as geek

# creating input array using 
# array function
in_arr = geek.array([[ 64, 128], [ 17, 25]], dtype = geek.uint8)
print ("Input array : ", in_arr) 

# unpacking elements of an array
# using unpackbits() function
out_arr = geek.unpackbits(in_arr, axis = 0)

print ("Output unpacked array along axis 0 : ", out_arr) 
```

**Output :**

```
Input array :  [[ 64 128]
 [ 17  25]]
Output unpacked array along axis 0 :  [[0 1]
 [1 0]
 [0 0]
 [0 0]
 [0 0]
 [0 0]
 [0 0]
 [0 0]
 [0 0]
 [0 0]
 [0 0]
 [1 1]
 [0 1]
 [0 0]
 [0 0]
 [1 1]]

```