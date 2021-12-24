# Python 中的 numpy.floor_divide()

> 原文:[https://www.geeksforgeeks.org/numpy-floor_divide-python/](https://www.geeksforgeeks.org/numpy-floor_divide-python/)

**numpy.floor_divide(arr1，arr2，/，out = **None** ，其中= **True** ，casting = ' **同类**'，order = ' **K** '，dtype = None** ):

第一个数组中的数组元素除以第二个数组中的元素(都是按元素进行的)。arr1 和 arr2 必须具有相同的形状。
相当于 Python **//运算符**，与 Python **%** (余数)配对，作用为 **b = a % b + b * (a // b)** 向上舍入。

**参数:**

```py
arr1     : [array_like]Input array or object which works as numerator.

arr2     : [array_like]Input array or object which works as denominator. 

out      : [ndarray, None, optional]Output array with same dimensions as
           Input array, placed with result.

**kwargs : Allows you to pass keyword variable length of argument to a function. 
            It is used when we want to handle named argument in a function.

where    : [array_like, optional]True value means to calculate the universal 
            functions(ufunc) at that position, False value means to leave the 
            value in the output alone.

```

**返回:**

```py
An array with floor(x1 / x2)

```

**代码 1 : arr1 除以 arr2**

```py
# Python program explaining
# floor_divide() function
import numpy as np

# input_array
arr1 = [2, 2, 2, 2, 2]
arr2 = [2, 3, 4, 5, 6]
print ("arr1         : ", arr1)
print ("arr1         : ", arr2)

# output_array
out = np.floor_divide(arr1, arr2)
print ("\nOutput array : ", out)
```

**输出:**

```py
arr1         :  [2, 2, 2, 2, 2]
arr1         :  [2, 3, 4, 5, 6]

Output array :  [1 0 0 0 0]

```

**代码 arr1 的元素除以除数**

```py
# Python program explaining
# floor_divide() function
import numpy as np

# input_array
arr1 = [2, 7, 3, 11, 4]
divisor = 3
print ("arr1         : ", arr1)

# output_array
out = np.floor_divide(arr1, divisor)
print ("\nOutput array : ", out)
```

**输出:**

```py
arr1         :  [2, 7, 3, 11, 4]

Output array :  [0 2 1 3 1]
```

**代码 3:如果 arr2 有-ve 元素**则 floor_divide 处理结果

```py
# Python program explaining
# floor_divide() function
import numpy as np

# input_array
arr1 = [2, 6, 21, 21, 12]
arr2 = [2, 3, 4, -3, 6]
print ("arr1         : ", arr1)
print ("arr2         : ", arr2)

# output_array
out = np.floor_divide(arr1, arr2)
print ("\nOutput array : ", out)
```

**输出:**

```py
arr1         :  [2, 6, 21, 21, 12]
arr2         :  [2, 3, 4, -3, 6]

Output array :  [ 1  2  5 -7  2]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . floor _ divide . html](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.floor_divide.html)
。