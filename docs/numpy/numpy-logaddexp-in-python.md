# python 中的 numpy . logaddexp()

> 原文:[https://www.geeksforgeeks.org/numpy-logaddexp-in-python/](https://www.geeksforgeeks.org/numpy-logaddexp-in-python/)

**numpy.logaddexp()** 函数用于计算输入的幂和的对数。

该函数在统计中非常有用，因为计算出的事件概率可能很小，超出了正常浮点数的范围。在这种情况下，存储计算出的概率的对数。这个函数允许添加以这种方式存储的概率。它计算`log(exp(arr1) + exp(arr2))`。

> **语法:** numpy.logaddexp(arr1，arr2，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，ufunc 'logaddexp ')
> 
> **参数:**
> **arr 1:**【array _ like】输入数组。
> **arr 2:**【array _ like】输入数组。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **其中:**【array _ like，可选】True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。
> ****kwargs :** 允许您将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时，会用到它。
> 
> **返回:**【数组或标量】返回 exp(arr1) + exp(arr2)的对数。如果 arr1 和 arr2 都是标量，这就是标量。

**代码#1 :**

```
# Python3 code demonstrate logaddexp() function

# importing numpy
import numpy as np

in_num1 = 2
in_num2 = 3
print ("Input  number1 : ", in_num1)
print ("Input  number2 : ", in_num2)

out_num = np.logaddexp(in_num1, in_num2)
print ("Output number : ", out_num)
```

**输出:**

```
Input  number1 :  2
Input  number2 :  3
Output number :  3.31326168752

```

**代码#2 :**

```
# Python3 code demonstrate logaddexp() function

# importing numpy
import numpy as np

in_arr1 = [2, 3, 8] 
in_arr2 = [1, 2, 3]
print ("Input array1 : ", in_arr1) 
print ("Input array2 : ", in_arr2)

out_arr = np.logaddexp(in_arr1, in_arr2) 
print ("Output array : ", out_arr) 
```

**输出:**

```
Input array1 :  [2, 3, 8]
Input array2 :  [1, 2, 3]
Output array :  [ 2.31326169  3.31326169  8.00671535]

```