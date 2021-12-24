# Python 中的 numpy.divide()

> 原文:[https://www.geeksforgeeks.org/numpy-divide-python/](https://www.geeksforgeeks.org/numpy-divide-python/)

**numpy.divide(arr1，arr2，out = None，其中= True，casting = 'same_kind '，order = 'K '，dtype = None) :**
第一个数组中的数组元素被第二个数组中的元素分割(所有操作都是按元素进行的)。arr1 和 arr2 必须具有相同的形状，arr2 中的元素不得为零；否则会引发错误。

**参数:**

> **arr 1:**【array _ like】输入作为被除数的数组或对象。
> **arr 2:**【array _ like】输入作为除数的数组或对象。
> **出:**【n 数组，可选】输出数组，与输入数组尺寸相同，
> 放置有结果。
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。
> 当我们想要处理函数中的命名参数时使用。
> **其中:**【array _ like，可选】True 值表示计算该位置的通用
> 函数(ufunc)，False 值表示将
> 值单独留在输出中。

**返回:**

```py
An array with arr1/arr2(element-wise) as elements of output array.

```

**代码 1 : arr1 除以 arr2 元素**

```py
# Python program explaining
# divide() function
import numpy as np

# input_array
arr1 = [2, 27, 2, 21, 23]
arr2 = [2, 3, 4, 5, 6]
print ("arr1         : ", arr1)
print ("arr2         : ", arr2)

# output_array
out = np.divide(arr1, arr2)
print ("\nOutput array : \n", out)
```

**输出:**

```py
arr1         :  [2, 27, 2, 21, 23]
arr2         :  [2, 3, 4, 5, 6]

Output array : 
 [ 1\.          9\.          0.5         4.2         3.83333333]

```

**代码 arr1 的元素除以除数**

```py
# Python program explaining
# divide() function
import numpy as np

# input_array
arr1 = [2, 27, 2, 21, 23]
divisor = 3
print ("arr1         : ", arr1)

# output_array
out = np.divide(arr1, divisor)
print ("\nOutput array : \n", out)
```

**输出:**

```py
arr1         :  [2, 27, 2, 21, 23]

Output array : 
 [ 0.66666667  9\.          0.66666667  7\.          7.66666667]
```

**代码 3:如果 arr2 有元素= 0** 则警告

```py
# Python program explaining
# divide() function
import numpy as np

# input_array
arr1 = [2, 27, 2, 21, 23]
arr2 = [2, 3, 0, 5, 6]
print ("arr1         : ", arr1)
print ("arr2         : ", arr2)

# output_array
out = np.divide(arr1, arr2)
print ("\nOutput array : ", out)
```

**输出:**

```py
arr1         :  [2, 27, 2, 21, 23]
arr2         :  [2, 3, 0, 5, 6]

Output array :  [ 1\.          9\.                 inf  4.2         3.83333333]
RuntimeWarning: divide by zero encountered in true_divide
  out = np.power(arr1, arr2)

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . divide . html](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.divide.html)
。