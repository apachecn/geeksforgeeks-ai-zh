# Python 中的 numpy.true_divide()

> 原文:[https://www.geeksforgeeks.org/numpy-true_divide-python/](https://www.geeksforgeeks.org/numpy-true_divide-python/)

**(arr1，arr22，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，ufunc 'true_divide') :**
第一个数组中的数组元素被第二个数组中的元素除(都是按元素进行的)。arr1 和 arr2 必须具有相同的形状。按元素返回真除法。

Python 传统上遵循“楼层划分”。无论输入类型如何，真正的除法都会将答案调整到最佳状态。
**”//**是楼层划分符。
**“/**是真师符。

**参数:**

```
arr1     : [array_like]Input array or object which works as numerator.
arr2     : [array_like]Input array or object which works as denominator. 
out      : [ndarray, None, optional]Output array with same dimensions as Input array, 
           placed with result.
**kwargs : allows you to pass keyword variable length of argument to a function. 
           It is used when we want to handle named argument in a function.
where    : [array_like, optional]True value means to calculate the universal 
           functions(ufunc) at that position, False value means to leave the  
           value in the output alone.

```

**返回:**

```
If inputs are scalar then scalar; otherwise array with arr1 / arr2(element- wise) 
i.e. true division

```

**代码 1 : arr1 除以 arr2**

```
# Python program explaining
# true_divide() function
import numpy as np

# input_array
arr1 = [6, 7, 2, 9, 1]
arr2 = [2, 3, 4, 5, 6]
print ("arr1         : ", arr1)
print ("arr1         : ", arr2)

# output_array
out = np.true_divide(arr1, arr2)
print ("\nOutput array : \n", out)
```

**输出:**

```
arr1         :  [6, 7, 2, 9, 1]
arr1         :  [2, 3, 4, 5, 6]

Output array : 
 [ 3\.          2.33333333  0.5         1.8         0.16666667]

```

**代码 arr1 的元素除以除数**

```
# Python program explaining
# true_divide() function
import numpy as np

# input_array
arr1 = [2, 7, 3, 11, 4]
divisor = 3
print ("arr1         : ", arr1)

# output_array
out = np.true_divide(arr1, divisor)
print ("\nOutput array : ", out)
```

**输出:**

```
arr1         :  [2, 7, 3, 11, 4]

Output array :  [ 0.66666667  2.33333333  1\.          3.66666667  1.33333333]
```

**代码 3:floor _ division(//)和 true-division(/**的比较

```
# Python program explaining
# true_divide() function
import numpy as np

# input_array
arr1 = np.arange(5)
arr2 = [2, 3, 4, 5, 6]
print ("arr1         : ", arr1)
print ("arr1         : ", arr2)

# output_array
out = np.floor_divide(arr1, arr2)
out_arr = np.true_divide(arr1, arr2) 
print ("\nOutput array with floor divide : \n", out)
print ("\nOutput array with true divide  : \n", out_arr)

print ("\nOutput array with floor divide(//) : \n", arr1//arr2)
print ("\nOutput array with true divide(/)   : \n", arr1/arr2)
```

**输出:**

```
arr1         :  [0 1 2 3 4]
arr1         :  [2, 3, 4, 5, 6]

Output array with floor divide : 
 [0 0 0 0 0]

Output array with true divide  : 
 [ 0\.          0.33333333  0.5         0.6         0.66666667]

Output array with floor divide(//) : 
 [0 0 0 0 0]

Output array with true divide(/)   : 
 [ 0\.          0.33333333  0.5         0.6         0.66666667]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . floor _ divide . html](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.floor_divide.html)
。