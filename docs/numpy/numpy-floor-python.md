# Python 中的 numpy.floor()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-floor-python/

**numpy.floor)** 是一个返回数组元素的 floor 的数学函数。标量 x 的底是最大的整数 I，这样 i < = x。

> **语法:** numpy.floor(x[，out]) = ufunc 'floor')
> **参数:**
> **a:***【array _ like】*输入数组
> 
> **返回:**各元素的楼层。

**代码#1:工作**

```
# Python program explaining
# floor() function

import numpy as np

in_array = [.5, 1.5, 2.5, 3.5, 4.5, 10.1]
print ("Input array : \n", in_array)

flooroff_values = np.floor(in_array)
print ("\nRounded values : \n", flooroff_values)

in_array = [.53, 1.54, .71]
print ("\nInput array : \n", in_array)

flooroff_values = np.floor(in_array)
print ("\nRounded values : \n", flooroff_values)

in_array = [.5538, 1.33354, .71445]
print ("\nInput array : \n", in_array)

flooroff_values = np.floor(in_array)
print ("\nRounded values : \n", flooroff_values)
```

**输出:**

```
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

**代码#2:工作**

```
# Python program explaining
# floor() function
import numpy as np

in_array = [1.67, 4.5, 7, 9, 12]
print ("Input array : \n", in_array)

flooroff_values = np.floor(in_array)
print ("\nRounded values : \n", flooroff_values)

in_array = [133.000, 344.54, 437.56, 44.9, 1.2]
print ("\nInput array : \n", in_array)

flooroff_values = np.floor(in_array)
print ("\nRounded values upto 2: \n", flooroff_values)
```

**输出:**

```
Input array : 
 [1.67, 4.5, 7, 9, 12]

Rounded values : 
 [  1\.   4\.   7\.   9\.  12.]

Input array : 
 [133.0, 344.54, 437.56, 44.9, 1.2]

Rounded values upto 2: 
 [ 133\.  344\.  437\.   44\.    1.]

```

**参考文献:**[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . floor . html # numpy . floor](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.floor.html#numpy.floor)
。