# numpy 字符串运算| less()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-less-function/](https://www.geeksforgeeks.org/numpy-string-operations-less-function/)

numpy . core . defchararray . less(arr 1，arr2)是 NumPy 中做字符串运算的另一个函数。它逐个检查两个相同形状的字符串数组的元素，如果 arr1 的元素少于 arr2 的元素，即 arr1 < arr2，则返回 *True* 。否则，返回*假*。

> **参数:**
> **arr1 :** 字符串或 unicode.1st 输入数组的 array_like。
> **arr2 :** 字符串或 unicode 的 array _ like . 2nd 输入数组。
> **返回:**【ndarray】bool 的输出数组，如果 arr1 和 arr2 是标量，则返回单个 bool。

**代码#1 :**

## 蟒蛇 3

```py
# Python program explaining
# numpy.char.less() method

# importing numpy
import numpy as geek

# input arrays 
in_arr1 = geek.array('numpy')
print ("1st Input array : ", in_arr1)

in_arr2 = geek.array('number')
print ("2nd Input array : ", in_arr2) 

# checking if in_arr1 < in_arr2
out_arr = geek.char.less(in_arr1, in_arr2)
print ("Output array: ", out_arr)
```

**Output:** 

```py
1st Input array :  numpy
2nd Input array :  number
Output array:  False
```

**代码#2 :**

## 蟒蛇 3

```py
# Python program explaining
# numpy.char.less() method

# importing numpy
import numpy as geek

# input arrays 
in_arr1 = geek.array(['Geeks', 'for', 'Geek', 'Numpy'])
print ("1st Input array : ", in_arr1)

in_arr2 = geek.array(['Geek', 'for', 'geek', 'numpy'])
print ("2nd Input array : ", in_arr2)

# checking if in_arr1 < in_arr2
out_arr = geek.char.less(in_arr1, in_arr2)
print ("Output array: ", out_arr)
```

**Output:** 

```py
1st Input array :  ['Geeks' 'for' 'Geek' 'Numpy']
2nd Input array :  ['Geek' 'for' 'geek' 'numpy']
Output array:  [False False  True  True]
```

**代码#3 :**

## 蟒蛇 3

```py
# Python program explaining
# numpy.char.less() method

# importing numpy
import numpy as geek

# input arrays 
in_arr1 = geek.array(['10', '11', '122', '15'])
print ("1st Input array : ", in_arr1)

in_arr2 = geek.array(['10', '13', '121', '141'])
print ("2nd Input array : ", in_arr2)

# checking if in_arr1 < in_arr2
out_arr = geek.char.less(in_arr1, in_arr2)
print ("Output array: ", out_arr)
```

**Output:** 

```py
1st Input array :  ['10' '11' '122' '15']
2nd Input array :  ['10' '13' '121' '141']
Output array:  [False  True False False]
```