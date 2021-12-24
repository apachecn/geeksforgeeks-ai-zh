# numpy.defchararray.center()用 Python

表示

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-defchararray-center-in-python/

**`numpy.core.defchararray.center(arr, width, fillchar)` :** 将字符串元素按元素排列。

> **参数:**
> **arr :** 阵状或弦状。
> **宽度:**结果字符串的长度。
> **填充字符:**填充字符。默认为空格。
> 
> **返回:**带中心字符串的数组副本。

**代码#1:**

```py
# Python Program illustrating 
# numpy.char.center() method 
import numpy as np 

arr1 = ['eAAAa', 'ttttds', 'AAtAAt']
print ("arr1 : ", arr1)

print ("\narr1 : ", np.char.center(arr1, 7, fillchar ='z'))
print ("\narr1 : ", np.char.center(arr1, [9, 9, 11],
                         fillchar =['z', '1', '3']))

print ("\narr1 : ", np.char.center(arr1, 11, fillchar ='z'))
```

**输出:**

```py
arr1 :  ['eAAAa', 'ttttds', 'AAtAAt']

 centered arr1 :  ['zeAAAaz' 'zttttds' 'zAAtAAt']

 centered arr1 :  ['zzeAAAazz' '11ttttds1' '333AAtAAt33']

 centered arr1 :  ['zzzeAAAazzz' 'zzzttttdszz' 'zzzAAtAAtzz']

```

**代码#2:**

```py
# Python Program illustrating 
# numpy.char.center() method 
import numpy as np 

arr2 = ['11sf', 'sdsf2', '1111f2']
print ("arr2 : ", arr2)

# Will throw Error
print ("\narr2 : ", np.char.center(arr2))
```

**输出:**

```py
arr2 :  ['11sf', 'sdsf2', '1111f2']

TypeError: center() missing 1 required positional argument: 'width'

```