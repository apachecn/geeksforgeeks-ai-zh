# python 中的 numpy.copysign()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-copy sign-in python/

**`numpy.copysign(arr1, arr2, out = None, where = True, casting = ‘same_kind’, order = ‘K’, dtype = None)` :** 这个数学函数帮助用户改变 arr1 和 arr2 的符号。arr1 或 arr2 都可以是列表/序列或标量值。如果顺序，两者必须具有相同的维度；否则 arr2 可以是标量值。

> **参数:**
> **arr 1:**【array _ like】输入数组，数值要变号。
> **arr 2:**【array _ like】输入数组，要改变符号的值。
> **输出:**【n 数组，可选】输出数组，与输入数组尺寸相同，与结果一起放置。
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。
> 
> **返回:** x1，符号为 x2。

**代码#1:**

```
# Python program illustrating 
# copysign() method 
import numpy as np 

arr1 = [1, -23, +34, 11]
arr2 = [-1, 2, -3, -4]

print ("arr1 : ", arr1)
print ("arr2 : ", arr2)

print ("\nCheck sign of arr1 : ", np.signbit(arr1))
print ("\nCheck sign of arr2 : ", np.signbit(arr1))
print ("\nCheck for copysign : ", np.signbit(np.copysign(arr1, arr2)))
```

**输出:**

```
arr1 :  [1, -23, 34, 11]
arr2 :  [-1, 2, -3, -4]

Check sign of arr1 :  [False  True False False]
Check sign of arr2 :  [False  True False False]
Check for copysign :  [ True False  True  True]

```

**代码#2:**

```
# Python program illustrating 
# copysign() method 
import numpy as np 

arr1 = [1, -23, +34, 11]

print ("\nCheck sign of arr2 : ", np.signbit(arr1))
print ("\nCheck for copysign : ", np.signbit(np.copysign(arr1, -3)))
```

**输出:**

```
Check sign of arr2 :  [False  True False False]
Check for copysign :  [ True  True  True  True]

```