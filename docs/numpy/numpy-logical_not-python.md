# Python 中的 numpy.logical _ not()

> 原文:[https://www.geeksforgeeks.org/numpy-logical_not-python/](https://www.geeksforgeeks.org/numpy-logical_not-python/)

**numpy . logic _ NOT(arr，out=None，其中= True，casting = 'same_kind '，order = 'K '，dtype = None，ufunc ' logic _ NOT '):**这是一个逻辑函数，按元素计算 **NOT** arr 的真值。

**参数:**

> **arr 1:**【array _ like】输入数组。
> 
> **输出:**【n 数组，可选】输出数组，与输入数组具有相同的尺寸，与结果一起放置。
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> 
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。

**返回:**

```
An array with Boolean results of NOT arr (element-wise).  

```

**代码 1:工作**

```
# Python program explaining
# logical_not() function
import numpy as np

# input
arr1 = [1, 3, False, 4]
arr2 = [3, 0, True, False]

# output
out_arr1 = np.logical_not(arr1)
out_arr2 = np.logical_not(arr2)

print ("Output Array 1 : ", out_arr1)
print ("Output Array 2 : ", out_arr2)
```

**输出:**

```
Output Array 1 :  [False False  True False]
Output Array 2 :  [False  True False  True]

```

**代码 2:可以检查条件**

```
# Python program explaining
# logical_not() function
import numpy as np

# input
arr1 = np.arange(8)

# Applying Condition 
print ("Output : \n", arr1/4)

# output
out_arr1 = np.logical_not(arr1/4 == 0)

print ("\n Boolean Output : \n", out_arr1)
```

**输出:**

```
Output : 
 [ 0\.    0.25  0.5   0.75  1\.    1.25  1.5   1.75]

 Boolean Output : 
 [False  True  True  True  True  True  True  True]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . logic _ not . html # numpy . logic _ not](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.logical_not.html#numpy.logical_not)
。