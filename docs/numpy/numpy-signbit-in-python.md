# python 中的 numpy.signbit()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-signabit-in-python/

**`numpy.signbit(array, out = None, where = True, casting = ‘same_kind’, order = ‘K’, dtype = None)` :** 该数学函数帮助用户逐元素检查 signbit 是否置位。

> **参数:**
> **数组:**【array _ like】输入数组或对象其元素，我们需要检查。
> **输出:**【n 数组，可选】与输入数组尺寸相同的输出数组，与结果一起放置。
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。
> 
> **返回:**真，如果设置了符号位；否则就是假的。

代码:

```
# Python program illustrating 
# signbit() method 

import numpy as np 

arr = [1, -23, +34, 11]
print ("arr : ", arr)

print ("\nCheck for signbit : ", np.signbit(arr))

out_arr = np.arange(4)
print ("\nout_arr : ", out_arr)

np.signbit(arr, out = out_arr)

print ("\nplacing signbit check values to out_arr : ", out_arr)
```

**输出:**

```
arr :  [1, -23, 34, 11]

Check for signbit :  [False  True False False]

out_arr :  [0 1 2 3]

placing signbit check values to out_arr :  [0 1 0 0]

```