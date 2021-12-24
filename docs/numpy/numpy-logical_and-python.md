# Python 中的 numpy.logical _ and()

> 原文:[https://www.geeksforgeeks.org/numpy-logical_and-python/](https://www.geeksforgeeks.org/numpy-logical_and-python/)

**numpy . logic _ AND(arr 1，arr2，out=None，其中= True，casting = 'same_kind '，order = 'K '，dtype = None，ufunc ' logic _ AND '):**这是一个逻辑函数，它帮助用户逐元素找出 arr1 **和** arr2 的真值。两个阵列必须具有相同的形状。

**参数:**

> **arr 1:**【array _ like】输入数组。
> **arr2 :** 【阵 _ 象】输入阵。
> 
> **输出:**【n 数组，可选】输出数组，与输入数组具有相同的尺寸，与结果一起放置。
> 
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> 
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。

**返回:**

```
An array with Boolean results of arr1 and arr2 element-wise(of the same shape).  

```

**代码 1:工作**

```
# Python program explaining
# logical_and() function
import numpy as np

# input
arr1 = [1, 3, False, 4]
arr2 = [3, 0, True, False]

# output
out_arr = np.logical_and(arr1, arr2)

print ("Output Array : ", out_arr)
```

**输出:**

```
Output Array :  [ True False False False]

```

**代码 2:如果输入数组的形状不同，则值错误**

```
# Python program explaining
# logical_and() function
import numpy as np

# input
arr1 = [8, 2, False, 4]
arr2 = [3, 0, True, False, 8]

# output
out_arr = np.logical_and(arr1, arr2)

print ("Output Array : ", out_arr)
```

**输出:**

```
<font color="red">ValueError:</font>operands could not be broadcast together with shapes (4,) (5,) 
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . logic _ and . html # numpy . logic _ and](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.logical_and.html#numpy.logical_and)
。