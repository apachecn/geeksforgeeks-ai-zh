# numpy 字符串运算| not_equal()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-not _ equal-function/](https://www.geeksforgeeks.org/numpy-string-operations-not_equal-function/)

`numpy.core.defchararray.not_equal(arr1, arr2)`是 numpy 中做字符串运算的另一个函数。它逐个检查两个相同形状数组的元素，如果它们不相等，则返回*真*。否则，返回*假*。

> **参数:**
> **arr1 :** 类似字符串或 unicode 的数组。
> **arr2 :** 字符串或 unicode 的 array_like。
> 
> **返回:**【ndarray】bool 的输出数组，如果 arr1 和 arr2 是标量，则返回单个 bool。

**代码#1 :**

```py
# Python program explaining
# numpy.char.not_equal() method 

# importing numpy 
import numpy as geek

# input arrays  
in_arr1 = geek.array('numpy')
print ("1st Input array : ", in_arr1)

in_arr2 = geek.array('nump')
print ("2nd Input array : ", in_arr2)  

# checking if they are not equal
out_arr = geek.char.not_equal(in_arr1, in_arr2)
print ("Output array: ", out_arr) 
```

**Output:**

```py
1st Input array :  numpy
2nd Input array :  nump
Output array:  True

```

**代码#2 :**

```py
# Python program explaining
# numpy.char.not_equal() method 

# importing numpy 
import numpy as geek

# input arrays  
in_arr1 = geek.array(['Geeks', 'for', 'Geeks'])
print ("1st Input array : ", in_arr1) 

in_arr2 = geek.array(['Geek', 'for', 'Geek'])
print ("2nd Input array : ", in_arr2) 

# checking if they are not equal
out_arr = geek.char.not_equal(in_arr1, in_arr2)
print ("Output array: ", out_arr) 
```

**Output:**

```py
1st Input array :  ['Geeks' 'for' 'Geeks']
2nd Input array :  ['Geek' 'for' 'Geek']
Output array:  [ True False  True]

```

**代码#3 :**

```py
# Python program explaining
# numpy.char.not_equal() method 

# importing numpy 
import numpy as geek

# input arrays  
in_arr1 = geek.array(['10', '11', '12'])
print ("1st Input array : ", in_arr1) 

in_arr2 = geek.array(['10', '11', '121'])
print ("2nd Input array : ", in_arr2) 

# checking if they are not equal
out_arr = geek.char.not_equal(in_arr1, in_arr2)
print ("Output array: ", out_arr) 
```

**Output:**

```py
1st Input array :  ['10' '11' '12']
2nd Input array :  ['10' '11' '121']
Output array:  [False False  True]

```