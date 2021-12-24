# Python 中的 numpy.array_equal()

> 原文:[https://www.geeksforgeeks.org/numpy-array_equal-python/](https://www.geeksforgeeks.org/numpy-array_equal-python/)

**numpy.array_equal(arr1，arr2) :** 检查两个数组是否具有相同形状和元素的逻辑函数。

**参数:**

```
arr1    : [array_like]Input array or object whose elements, we need to test.
arr2    : [array_like]Input array or object whose elements, we need to test.

```

**返回:**

```
True, if both arrays have same shape and value; otherwise False

```

**代码:解释工作**

```
# Python program explaining
# array_equal() function
import numpy as np

# input
arr1 = np.arange(4)
arr2 = [7, 4, 6, 7]
print ("arr1 : ", arr1)
print ("arr2 : ", arr2)

print ("\nResult : ", np.array_equal(arr1, arr2))

arr1 = np.arange(4)
arr2 = np.arange(4)
print ("\n\narr1 : ", arr1)
print ("arr2 : ", arr2)

print ("\nResult : ", np.array_equal(arr1, arr2))

arr1 = np.arange(4)
arr2 = np.arange(5)
print ("\n\narr1 : ", arr1)
print ("arr2 : ", arr2)

print ("\nResult : ", np.array_equal(arr1, arr2))
```

**输出:**

```
arr1 :  [0 1 2 3]
arr2 :  [7, 4, 6, 7]

Result :  False

arr1 :  [0 1 2 3]
arr2 :  [0 1 2 3]

Result :  True

arr1 :  [0 1 2 3]
arr2 :  [0 1 2 3 4]

Result :  False

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . array _ equal . html](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.array_equal.html)
。