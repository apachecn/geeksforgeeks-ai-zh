# num py . defchararray . capitalize()用 Python

表示

> 原文:[https://www . geesforgeks . org/numpy-defchararray-大写-in-python/](https://www.geeksforgeeks.org/numpy-defchararray-capitalize-in-python/)

**numpy . core . defchararray . multiply(arr，n):** 按元素将字符串的第一个字母大写。

> **参数:**
> **arr :** 阵状或弦状。
> 
> **返回:**字符串的首字母大写。

**代码#1:**

```py
# Python Program illustrating 
# numpy.char.capitalize() method 
import numpy as np 

arr1 = ['eAAAaeAAAa', 'ttttdsttttds', 'AAtAAt']
arr2 = ['11sf', 'sdsf2', '1111f2']

print ("arr1 : ", arr1)
print ("arr2 : ", arr2)

Print("\nArrays after using capitalize():")
print ("\narr1 : ", np.char.capitalize(arr1))
print ("arr2 : ", np.char.capitalize(arr2))
```

**输出:**

```py
arr1 :  ['eAAAaeAAAa', 'ttttdsttttds', 'AAtAAt']
arr2 :  ['11sf', 'sdsf2', '1111f2']

Arrays after using capitalize():
arr1 :  ['Eaaaaeaaaa' 'Ttttdsttttds' 'Aataat']
arr2 :  ['11sf' 'Sdsf2' '1111f2']

```

**代码#2:**

```py
# Python Program illustrating 
# numpy.char.capitalize() method 
import numpy as np 

arr1 = 'this is geeks '
arr2 = 'for geeks '

print ("arr1 : ", arr1)
print ("arr2 : ", arr2)

Print("\nArrays after using capitalize():")
print ("\narr1 : ", np.char.capitalize(arr1))
print ("arr2 : ", np.char.capitalize(arr2))
```

**输出:**

```py
arr1 :  this is geeks 
arr2 :  for geeks 

Arrays after using capitalize():
arr1 :  This is geeks 
arr2 :  For geeks  

```