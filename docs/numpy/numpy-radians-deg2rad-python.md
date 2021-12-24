# Python 中的 numpy .弧度()和 deg2rad()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-radians-deg2 rad-python/

**numpy.radians()** 是一个数学函数，帮助用户将角度从度数转换为弧度。

> **语法:** numpy.radians(x[，out]) = ufunc 'radians')
> **参数:**
> 
> **阵:** *【阵 _ 象】*元素以度为单位。
> **出:***【ndaaray，可选】*输出数组的形状与 x 相同。
> 2pi 弧度= 36o 度
> 
> **返回:**用弧度值代替度数值的数组。

**代码#1:工作**

```
# Python3 program explaining
# degrees() function

import numpy as np
import math

in_array = np.arange(10.) * 90
print ("Degree values : \n", in_array)

radian_Values = np.radians(in_array)
print ("\nRadian values : \n", radian_Values)
```

**输出:**

```
Degree values : 
 [   0\.   90\.  180\.  270\.  360\.  450\.  540\.  630\.  720\.  810.]

Radian values : 
 [  0\.           1.57079633   3.14159265   4.71238898   6.28318531
   7.85398163   9.42477796  10.99557429  12.56637061  14.13716694]

```

**numpy.deg2rad(x[，out]) = ufunc 'deg2rad') :** 此数学函数可帮助用户将角度从度数转换为弧度

> **参数:**
> 
> **数组:***【array _ like】*元素以弧度为单位。
> **出:***【ndaaray，可选】*输出数组的形状与 x 相同。
> 2pi 弧度= 36o 度
> 
> **返回:**弧度对应角度。

**代码#2 : deg2rad()相当于弧度()**

```
# Python3 program explaining
# rad2deg() function

import numpy as np
import math

degree = np.arange(10.) * 90
print ("Degree values : \n", degree)

radian = np.deg2rad(degree)
print ("\nradian values : \n", radian)
```

**输出:**

```
Degree values : 
 [   0\.   90\.  180\.  270\.  360\.  450\.  540\.  630\.  720\.  810.]

radian values : 
 [  0\.           1.57079633   3.14159265   4.71238898   6.28318531
   7.85398163   9.42477796  10.99557429  12.56637061  14.13716694]

```

**参考文献:**[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . radians . html # numpy . radians](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.radians.html#numpy.radians)
。