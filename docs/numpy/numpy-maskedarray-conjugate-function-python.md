# Numpy maskearray .共轭()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-masked array-共轭-函数-python/](https://www.geeksforgeeks.org/numpy-maskedarray-conjugate-function-python/)

**`numpy.MaskedArray.conjugate()`** 函数用于返回复共轭，元素式。复数的共轭是通过改变其虚部的符号得到的。

> **语法:** `numpy.ma.conjugate(arr, out=None, where=True, casting='same_kind', order='K', dtype=None, subok=True)`
> 
> **参数:**
> 
> **arr:**【array _ like】输入我们想要共轭的屏蔽数组。
> **出:**【可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **其中:**【array _ like，可选】值为 True 表示计算该位置的 ufunc，值为 False 表示将该值单独留在输出中。
> **铸造:** [ 'no '，' equiv '，' safe '，' same_kind '，或' unsafe']提供了允许哪种铸造的策略。
> **顺序:**使用这个索引顺序读取一个的元素。
> **数据类型:**【数据类型，可选】返回数组的类型，以及元素相乘的累加器的类型。
> **subok :** 默认为真。如果设置为 false，输出将始终是严格数组，而不是子类型。
> 
> **返回:**【ndarray】arr 的复共轭。

**代码#1 :**

```py
# Python program explaining
# numpy.MaskedArray.conjugate() method 

# importing numpy as geek  
# and numpy.ma module as ma 
import numpy as geek 
import numpy.ma as ma 

# creating input array  
in_arr = geek.array([[1 + 2j, 2 + 3j], [ 3-2j, -1 + 2j], [ 5-4j, -3-3j]])
print ("Input array : ", in_arr) 

# Now we are creating a masked array. 
# by making two entry as invalid.  
mask_arr = ma.masked_array(in_arr, mask =[[1, 0], [ 1, 0], [ 0, 0]]) 
print ("Masked array : ", mask_arr) 

# applying MaskedArray.conjugate    
# methods to masked array
out_arr = ma.conjugate(mask_arr) 
print ("conjugate of masked array : ", out_arr) 
```

**Output:**

```py
Input array :  [[ 1.+2.j  2.+3.j]
 [ 3.-2.j -1.+2.j]
 [ 5.-4.j -3.-3.j]]
Masked array :  [[-- (2+3j)]
 [-- (-1+2j)]
 [(5-4j) (-3-3j)]]
conjugate of masked array :  [[-- (2-3j)]
 [-- (-1-2j)]
 [(5+4j) (-3+3j)]

```