# python 中的 numpy.nextafter()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-nextafter-in-python/

**`numpy.nextafter(arr1, arr2, out = None, where = True, casting = ‘same_kind’, order = ‘K’, dtype = None)` :** 这个数学函数帮助用户按元素返回 arr1 之后的下一个浮点值。

> **参数:**
> **arr 1:**【array _ like】输入数组，值查找下一个值的。
> **arr 2:**【array _ like】输入数组，要查找哪个方向的值。
> **输出:**【n 数组，可选】输出数组，与输入数组尺寸相同，与结果一起放置。
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。
> 
> **返回:**arr 2 方向上 arr1 的下一个浮点值。

代码:

```py
# Python program illustrating 
# nextafter() method 
import numpy as np 

arr1 = 3
arr2 = 4

print ("arr1 : ", arr1)
print ("arr2 : ", arr2)

print ("\nCheck sign of arr1 : ", np.nextafter(arr1, arr2))
```

**输出:**

```py
arr1 :  3
arr2 :  4

Check sign of arr1 :  3.0000000000000004

```