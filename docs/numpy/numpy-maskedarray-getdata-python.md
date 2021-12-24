# numpy mask array . getdata()–python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-masked array-getdata-python/

**`numpy.ma.getdata()`** 函数用于将屏蔽数组的数据作为数组返回。如果 arr 是 MaskedArray，将 arr 的数据作为一个数组返回，否则将 arr 作为一个数组或子类返回。

> **语法** numpy.ma.getdata(a，subok=True)
> 
> **参数:**
> **arr:**【array _ like】输入掩码数组，或者是一个数组或其子类。
> **subok:**【bool】是强制输出为纯数组(False)还是返回数组的子类(True，默认值)。
> 
> **返回:**【n 数组】将屏蔽数组的数据作为 n 数组返回。

**代码#1 :**

```py
# Python program explaining
# numpy.ma.getdata() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma

arr = ma.masked_equal([[2, 4], [6, 8]], 4)
print("Input array : ", arr)

# applying numpy.ma.getdata() method
gfg = ma.getdata(arr)
print("Output array : ", gfg)
```

**输出:**

```py
Input array :  [[2 --]
 [6 8]]
Output array :  [[2 4]
 [6 8]]

```

**代码#2 :**

```py
# Python program explaining
# numpy.ma.getdata() function

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma

arr = ma.masked_equal([[1, 3], [5, 8]], 5)
print("Input array : ", arr)

# applying numpy.ma.getdata() method
gfg = ma.getdata(arr)
print("Output array : ", gfg)
```

**输出:**

```py
Input array :  [[1 3]
 [-- 8]]
Output array :  [[1 3]
 [5 8]]

```