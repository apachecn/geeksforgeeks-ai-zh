# Python 中的 numpy.array_equiv()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-array _ equiv-pyhton/

**numpy.array_equiv(arr1，arr2) :** 检查两个数组是否有相同元素且形状一致的逻辑函数。

**形状一致**表示它们具有相同的形状，或者一个输入数组可以被广播以创建与另一个相同的形状。

**参数:**

```
arr1    : [array_like]Input array, we need to test.
arr2    : [array_like]Input array, we need to test.

```

**返回:**

```
True, if both arrays are equivalent; otherwise False

```

**代码:解释工作**

```
# Python program explaining
# array_equiv() function
import numpy as np

# input
arr1 = np.arange(4)
arr2 = [7, 4, 6, 7]
print ("arr1 : ", arr1)
print ("arr2 : ", arr2)

print ("\nResult : ", np.array_equiv(arr1, arr2))

arr1 = np.arange(4)
arr2 = np.arange(4)
print ("\n\narr1 : ", arr1)
print ("arr2 : ", arr2)

print ("\nResult : ", np.array_equiv(arr1, arr2))

arr1 = np.arange(4)
arr2 = np.arange(5)
print ("\n\narr1 : ", arr1)
print ("arr2 : ", arr2)

print ("\nResult : ", np.array_equiv(arr1, arr2))

a = np.array_equiv([1, 2], [[1, 2, 1, 2], [1, 2, 1, 2]])

b = np.array_equiv([1, 2], [[1, 2], [1, 2]])

print ("\n\na : ", a)
print ("\nb : ", b)
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

a :  False

b :  True

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . array _ equiv . html # numpy . array _ equiv](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.array_equiv.html#numpy.array_equiv)
。