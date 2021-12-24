# Python 中的 numpy . pack bits()

> 原文:[https://www.geeksforgeeks.org/numpy-packbits-in-python/](https://www.geeksforgeeks.org/numpy-packbits-in-python/)

**`numpy.packbits()`** 是 numpy 中做二进制运算的另一个函数。它用于将二进制值数组的元素打包成 uint8 数组中的位。通过在末尾插入零位，将结果填充为完整字节。

> **语法:** numpy.packbits(arr，axis=None)
> 
> **参数:**
> **arr:**【array _ like】整数或布尔值的数组，其元素应该被打包成位。
> **轴:**【int，可选】完成位填充的尺寸。如果没有，则打包成扁平数组。
> 
> **返回:**【打包数组】uint8 类型的数组，其元素表示对应于输入元素的逻辑(0 或非零)值的位。

**代码#1 :**

```py
# Python program explaining
# numpy.packbits() function

# importing numpy
import numpy as geek

# creating input array using 
# array function
in_arr = geek.array([[[1, 0, 1],
                     [0, 1, 0]],
                     [[1, 1, 0],
                        [0, 0, 1]]])
print ("Input array : ", in_arr) 

# packing elements of an array
# using packbits() function
out_arr = geek.packbits(in_arr)

print ("Output packed array : ", out_arr)
```

**Output :**

```py
Input array :  
[[[1 0 1]
  [0 1 0]]

 [[1 1 0]
  [0 0 1]]]
Output packed array :  [171  16]

```

**代码#2 :**

```py
# Python program explaining
# numpy.packbits() function

# importing numpy
import numpy as geek

# creating input array using 
# array function
in_arr = geek.array([[[0, 0, 1],
                     [1, 1, 0]],
                     [[1, 0, 0],
                        [1, 1, 1]]])
print ("Input array : ", in_arr) 

# packing elements of an array
# using packbits() function
out_arr = geek.packbits(in_arr, axis = 1)

print ("Output packed array along axis 1 : ", out_arr) 
```

**Output :**

```py
Input array :  [[[0 0 1]
  [1 1 0]]

 [[1 0 0]
  [1 1 1]]]
Output packed array along axis 1 :  [[[ 64  64 128]]

 [[192  64  64]]]

```