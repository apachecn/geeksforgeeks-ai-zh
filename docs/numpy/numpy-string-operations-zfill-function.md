# numpy 字符串操作| zfill()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-z fill-function/](https://www.geeksforgeeks.org/numpy-string-operations-zfill-function/)

`numpy.core.defchararray.zfill(arr, width)`是 numpy 中做字符串运算的另一个函数。对于数组中的每个元素，它返回左填充零的数字字符串。左填充零的数量根据宽度而定。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。输入数组。
> **宽度:**【int】填零后字符串的最终宽度。
> 
> **根据输入类型，返回字符串或 unicode 的输出数组。**

**代码#1 :**

```py
# Python program explaining
# numpy.char.zfill() method 

# importing numpy 
import numpy as geek

# input array  
in_arr = geek.array(['Geeks', 'for', 'Geeks'])
print ("Input array : ", in_arr) 

# setting the width of each string to 8
width = 8

# output array
out_arr = geek.char.zfill(in_arr, width)
print ("Output array: ", out_arr) 
```

**Output:**

```py
Input array :  ['Geeks' 'for' 'Geeks']
Output array:  ['000Geeks' '00000for' '000Geeks']

```

**代码#2 :**

```py
# Python program explaining
# numpy.char.zfill() method 

# importing numpy 
import numpy as geek

# input array  
in_arr = geek.array(['1', '11', '111'])
print ("Input array : ", in_arr)

# setting the width of each string to 5
width = 5

# output array
out_arr = geek.char.zfill(in_arr, width)
print ("Output array: ", out_arr) 
```

**Output:**

```py
Input array :  ['1' '11' '111']
Output array:  ['00001' '00011' '00111']

```