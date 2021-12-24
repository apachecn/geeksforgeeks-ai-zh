# Python 中的 numpy.ceil()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-ceil-python/

**numpy.ceil()** 是一个数学函数，返回数组元素的 ceil。标量 x 的上限是最小整数 I，这样 i > = x

> **语法:** numpy.ceil(x[，out]) = ufunc 'ceil')
> **参数:**
> **a:***【array _ like】*输入数组
> 
> **返回:**浮点数据类型的每个元素的上限。

**代码#1:工作**

```
# Python program explaining
# ceil() function
import numpy as np

in_array = [.5, 1.5, 2.5, 3.5, 4.5, 10.1]
print ("Input array : \n", in_array)

ceiloff_values = np.ceil(in_array)
print ("\nRounded values : \n", ceiloff_values)

in_array = [.53, 1.54, .71]
print ("\nInput array : \n", in_array)

ceiloff_values = np.ceil(in_array)
print ("\nRounded values : \n", ceiloff_values)

in_array = [.5538, 1.33354, .71445]
print ("\nInput array : \n", in_array)

ceiloff_values = np.ceil(in_array)
print ("\nRounded values : \n", ceiloff_values)
```

**输出:**

```
Input array : 
 [0.5, 1.5, 2.5, 3.5, 4.5, 10.1]

Rounded values : 
 [  1\.   2\.   3\.   4\.   5\.  11.]

Input array : 
 [0.53, 1.54, 0.71]

Rounded values : 
 [ 1\.  2\.  1.]

Input array : 
 [0.5538, 1.33354, 0.71445]

Rounded values : 
 [ 1\.  2\.  1.]

```

**代码#2:工作**

```
# Python program explaining
# ceil() function
import numpy as np

in_array = [1.67, 4.5, 7, 9, 12]
print ("Input array : \n", in_array)

ceiloff_values = np.ceil(in_array)
print ("\nRounded values : \n", ceiloff_values)

in_array = [133.000, 344.54, 437.56, 44.9, 1.2]
print ("\nInput array : \n", in_array)

ceiloff_values = np.ceil(in_array)
print ("\nRounded values upto 2: \n", ceiloff_values)
```

**输出:**

```
Input array : 
 [1.67, 4.5, 7, 9, 12]

Rounded values : 
 [  2\.   5\.   7\.   9\.  12.]

Input array : 
 [133.0, 344.54, 437.56, 44.9, 1.2]

Rounded values upto 2: 
 [ 133\.  345\.  438\.   45\.    2.]
```

**参考文献:**[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . ceil . html # numpy . ceil](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.ceil.html#numpy.ceil)
。