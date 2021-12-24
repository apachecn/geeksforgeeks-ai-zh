# Python 中的 numpy.float_power()

> 原文:[https://www.geeksforgeeks.org/numpy-float_power-python/](https://www.geeksforgeeks.org/numpy-float_power-python/)

**numpy.float_power(arr1，arr2，out = None，其中= True，casting = 'same_kind '，order = 'K '，dtype = None) :**
第一个数组中的数组元素被提升为第二个元素中的元素的幂(都是按元素进行的)。arr1 和 arr2 必须具有相同的形状。
**float_power** 与幂函数的不同之处在于，整数 float16 和 float32 被提升为 float64 的最小精度的浮点数，因此结果总是不精确的。这个函数将返回负幂的可用结果，对于+ve 幂很少溢出。

**参数:**

```
arr1     : [array_like]Input array or object which works as base.
arr2     : [array_like]Input array or object which works as exponent. 
out      : [ndarray, optional]Output array with same dimensions as Input array, 
            placed with result.
**kwargs : Allows you to pass keyword variable length of argument to a function. 
           It is used when we want to handle named argument in a function.
where    : [array_like, optional]True value means to calculate the universal 
           functions(ufunc) at that position, False value means to leave the 
           value in the output alone.

```

**返回:**

```
An array with elements of arr1 raised to exponents in arr2

```

**代码 1 : arr1 升至 arr2**

```
# Python program explaining
# float_power() function
import numpy as np

# input_array
arr1 = [2, 2, 2, 2, 2]
arr2 = [2, 3, 4, 5, 6]
print ("arr1         : ", arr1)
print ("arr1         : ", arr2)

# output_array
out = np.float_power(arr1, arr2)
print ("\nOutput array : ", out)
```

**输出:**

```
arr1         :  [2, 2, 2, 2, 2]
arr1         :  [2, 3, 4, 5, 6]

Output array :  [  4\.   8\.  16\.  32\.  64.]

```

**代码 arr1 的元素提升到指数 2**

```
# Python program explaining
# float_power() function
import numpy as np

# input_array
arr1 = np.arange(8)
exponent = 2
print ("arr1         : ", arr1)

# output_array
out = np.float_power(arr1, exponent)
print ("\nOutput array : ", out)
```

**输出:**

```
arr1         :  [0 1 2 3 4 5 6 7]

Output array :  [  0\.   1\.   4\.   9\.  16\.  25\.  36\.  49.]
```

**代码 3:如果 arr2 有-ve 元素**则 float_power 处理结果

```
# Python program explaining
# float_power() function
import numpy as np

# input_array
arr1 = [2, 2, 2, 2, 2]
arr2 = [2, -3, 4, -5, 6]
print ("arr1         : ", arr1)
print ("arr2         : ", arr2)

# output_array
out = np.float_power(arr1, arr2)
print ("\nOutput array : ", out)
```

**输出:**

```
arr1         :  [2, 2, 2, 2, 2]
arr2         :  [2, -3, 4, -5, 6]

Output array :  [  4.00000000e+00   1.25000000e-01   1.60000000e+01   
                3.12500000e-02   6.40000000e+01]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . float _ power . html # numpy . float _ power](//docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.float_power.html#numpy.float_power)
。