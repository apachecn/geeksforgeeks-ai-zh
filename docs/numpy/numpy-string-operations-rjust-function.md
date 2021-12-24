# numpy 字符串操作| rjust()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-rjust-function/](https://www.geeksforgeeks.org/numpy-string-operations-rjust-function/)

`numpy.core.defchararray.rjust(arr, width, fillchar=' ')`是 numpy 中做字符串运算的另一个函数。它返回一个数组，数组中 arr 的元素在长度和宽度的字符串中右对齐。它使用`fillchr`参数填充每个数组元素的剩余空间。如果`fillchr`没有通过，那么它用空格填充剩余的空间。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。输入数组。
> **宽度:**每根弦的最终宽度。
> **fillchar :** 要填充剩余空间的字符。
> 
> **返回:**【ndarray】输出字符串或 unicode 的右对齐数组，具体取决于输入类型。

**代码#1 :**

```py
# Python program explaining
# numpy.char.rjust() method 

# importing numpy 
import numpy as geek

# input array  
in_arr = geek.array(['Numpy', 'Python', 'Pandas'])
print ("Input array : ", in_arr) 

# setting the width of each string to 8
width = 8

# output array when fillchar is not passed
out_arr = geek.char.rjust(in_arr, width)
print ("Output right justified array: ", out_arr) 
```

**Output:**

```py
Input array :  ['Numpy' 'Python' 'Pandas']
Output right justified array:  ['   Numpy' '  Python' '  Pandas']

```

**代码#2 :**

```py
# Python program explaining
# numpy.char.rjust() method 

# importing numpy 
import numpy as geek

# input array  
in_arr = geek.array(['Numpy', 'Python', 'Pandas'])
print ("Input array : ", in_arr) 

# setting the width of each string to 8
width = 8

# output array 
out_arr = geek.char.rjust(in_arr, width, fillchar ='*')
print ("Output right justified array: ", out_arr) 
```

**Output:**

```py
Input array :  ['Numpy' 'Python' 'Pandas']
Output right justified array:  ['***Numpy' '**Python' '**Pandas']

```

**代码#3 :**

```py
# Python program explaining
# numpy.char.rjust() method 

# importing numpy 
import numpy as geek

# input array  
in_arr = geek.array(['1', '11', '111'])
print ("Input array : ", in_arr)

# setting the width of each string to 5
width = 5

# output array
out_arr = geek.char.rjust(in_arr, width, fillchar ='-')
print ("Output right justified array: ", out_arr) 
```

**Output:**

```py
Input array :  ['1' '11' '111']
Output right justified array:  ['----1' '---11' '--111']

```