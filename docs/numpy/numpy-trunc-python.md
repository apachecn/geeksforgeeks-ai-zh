# python 中的 numpy . trunc()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-truc-python/

**numpy.trunc()** 是一个数学函数，返回数组元素的截断值。标量 x 的中心是最接近的整数 I，比 x 更接近零。这简单地意味着，有符号数 x 的小数部分被这个函数丢弃。

> **语法:** numpy.trunc(x[，out]) = ufunc 'trunc')
> **参数:**
> 
> **a :** *【阵 _ 象】*输入阵
> 
> **返回:**
> 每个元素的截断，带有浮点数据类型

**代码#1:工作**

```py
# Python program explaining
# trunc() function

import numpy as np

in_array = [.5, 1.5, 2.5, 3.5, 4.5, 10.1]
print ("Input array : \n", in_array)

truncoff_values = np.trunc(in_array)
print ("\nRounded values : \n", truncoff_values)

in_array = [.53, 1.54, .71]
print ("\nInput array : \n", in_array)

truncoff_values = np.trunc(in_array)
print ("\nRounded values : \n", truncoff_values)

in_array = [.5538, 1.33354, .71445]
print ("\nInput array : \n", in_array)

truncoff_values = np.trunc(in_array)
print ("\nRounded values : \n", truncoff_values)
```

**输出:**

```py
Input array : 
 [0.5, 1.5, 2.5, 3.5, 4.5, 10.1]

Rounded values : 
 [  0\.   1\.   2\.   3\.   4\.  10.]

Input array : 
 [0.53, 1.54, 0.71]

Rounded values : 
 [ 0\.  1\.  0.]

Input array : 
 [0.5538, 1.33354, 0.71445]

Rounded values : 
 [ 0\.  1\.  0.]
```

**代码 2:工作**

```py
# Python program explaining
# trunc() function

import numpy as np

in_array = [1.67, 4.5, 7, 9, 12]
print ("Input array : \n", in_array)

truncoff_values = np.trunc(in_array)
print ("\nRounded values : \n", truncoff_values)

in_array = [133.000, 344.54, 437.56, 44.9, 1.2]
print ("\nInput array : \n", in_array)

truncoff_values = np.trunc(in_array)
print ("\nRounded values upto 2: \n", truncoff_values)
```

**输出:**

```py
Input array : 
 [1.67, 4.5, 7, 9, 12]

Rounded values : 
 [  1\.   4\.   7\.   9\.  12.]

Input array : 
 [133.0, 344.54, 437.56, 44.9, 1.2]

Rounded values upto 2: 
 [ 133\.  344\.  437\.   44\.    1.]
```

**参考文献:**[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . trunc . html # numpy . trunc](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.trunc.html#numpy.trunc)
。