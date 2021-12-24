# Python 中的 numpy.in1d()函数

> 原文:[https://www . geeksforgeeks . org/numpy-in1d-python 中的函数/](https://www.geeksforgeeks.org/numpy-in1d-function-in-python/)

**`numpy.in1d()`** 函数测试一维数组的每个元素是否也存在于第二个数组中，并返回一个与 arr1 长度相同的布尔数组，即 arr1 的元素在 arr2 中时为真，否则为假。

> **语法:** numpy.in1d(arr1，arr2，假定 _unique = False，invert = False)
> 
> **参数:**
> **arr 1:**【array _ like】输入数组。
> **arr 2:**【array _ like】测试 arr1 每个值的值。
> **假设 _ 唯一:**【bool，可选】如果为 True，则输入数组都假设为唯一，这样可以加快计算速度。默认值为假。
> **反转:**【bool，可选】如果为 True，则返回数组中的值反转。默认值为假。
> 
> **返回:**【ndarray，bool】arr 1[in1d]的值在 arr2 中。

**代码#1 :**

```py
# Python program explaining
# numpy.in1d() function

# importing numpy as geek 
import numpy as geek 

arr1 = geek.array([0, 1, 2, 3, 0, 4, 5])
arr2 = [0, 2, 5]

gfg = geek.in1d(arr1, arr2)

print (gfg)
```

**输出:**

```py
[ True False True False True False True]

```

**代码#2 :**

```py
# Python program explaining
# numpy.in1d() function

# importing numpy as geek 
import numpy as geek 

arr1 = geek.array([0, 1, 2, 3, 0, 4, 5])
arr2 = [0, 2, 5]

gfg = geek.in1d(arr1, arr2, invert = True)

print (gfg)
```

**输出:**

```py
[False True False True False True False]

```