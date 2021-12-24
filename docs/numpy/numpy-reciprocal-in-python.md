# Python 中的 numpy .倒数()

> 原文:[https://www.geeksforgeeks.org/numpy-reciprocal-in-python/](https://www.geeksforgeeks.org/numpy-reciprocal-in-python/)

**numpy .倒数()**是一个数学函数，用于计算输入数组中所有元素的倒数。

> **语法:** numpy .倒数(x，/，out=None，*，其中=True)
> **参数:**
> 
> **x**【array _ like】**:**输入需要测试元素的数组或对象。
> 
> **出**【ndarray，可选】 **:** 存储结果的位置。
> **–>**如果提供，它必须具有输入广播到的形状。
> **–>**如果未提供或无，则返回新分配的阵列。
> 
> ****kwargs :** 允许将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时使用。
> 
> **其中【array_like，可选】:** True 值表示计算该位置的通用函数(ufunc)，False 值表示将值单独留在输出中。
> 
> **返回:**
> **y :** ndarray。如果 x 是标量，这就是标量。

**注意:**对于绝对值大于 1 的整数参数，由于 Python 处理整数除法的方式，结果始终为零。对于整数零，结果是溢出。

**代码#1 :**

```py
# Python3 code demonstrate reciprocal() function

# importing numpy
import numpy as np

in_num = 2.0
print ("Input  number : ", in_num)

out_num = np.reciprocal(in_num)
print ("Output number : ", out_num)
```

**输出:**

```py
Input  number :  2.0
Output number :  0.5
```

**代码#2 :**

```py
# Python3 code demonstrate reciprocal() function

# importing numpy
import numpy as np

in_arr = [2., 3., 8.] 
print ("Input array : ", in_arr) 

out_arr = np.reciprocal(in_arr) 
print ("Output array : ", out_arr) 
```

**输出:**

```py
Input array :  [2.0, 3.0, 8.0]
Output array :  [ 0.5         0.33333333  0.125     ]
```

**代码#3 :** 倒数()函数异常。结果总是零。

```py
# Python3 code demonstrate Exception in reciprocal() function

# importing numpy
import numpy as np

in_arr = [2, 3, 8] 
print ("Input array : ", in_arr) 

out_arr = np.reciprocal(in_arr) 
print ("Output array : ", out_arr) 
```

**输出:**

```py
Input array :  [2, 3, 8]
Output array :  [0 0 0]

```