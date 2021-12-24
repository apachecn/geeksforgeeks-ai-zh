# Python 中的 numpy.degrees()和 rad2deg()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-degrees-rad 2 deg-python/

**numpy.degrees()** 是一个数学函数，帮助用户将角度从弧度转换为度数。

> **语法:** numpy.degrees(x[，out]) = ufunc 'degrees')
> **参数:**
> 
> **数组:***【array _ like】*元素以弧度为单位。
> **出:***【ndaaray，可选】*输出数组的形状与 x 相同。
> 2pi 弧度= 360 度
> 
> **返回:**用度数值代替弧度值的数组。

**代码#1:工作**

```
# Python3 program explaining
# degrees() function
import numpy as np
import math

in_array = [0, math.pi / 2, np.pi / 3, np.pi]
print ("Radian values : \n", in_array)

degree_Values = np.degrees(in_array)
print ("\nDegree values : \n", degree_Values)
```

**输出:**

```
Radian values : 
 [0, 1.5707963267948966, 1.0471975511965976, 3.141592653589793]

Degree values : 
 [   0\.   90\.   60\.  180.]

```

**numpy.rad2deg(x[，out]) = ufunc 'rad2deg') :** 此数学函数帮助用户将角度从弧度转换为度数。

> **参数:**
> 
> **数组:***【array _ like】*元素以弧度为单位。
> **出:***【ndaaray，可选】*输出数组的形状与 x 相同。
> 2pi 弧度= 36o 度
> 
> **返回:**对应角度的度数。

**代码#2 : rad2deg()相当于度数()**

```
# Python3 program explaining
# rad2deg() function

import numpy as np
import math

in_array = [0, math.pi / 2, np.pi / 3, np.pi]
print ("Radian values : \n", in_array)

out_Values = np.rad2deg(in_array)
print ("\nDegree values : \n", out_Values)
```

**输出:**

```
Radian values : 
 [0, 1.5707963267948966, 1.0471975511965976, 3.141592653589793]

Degree values : 
 [   0\.   90\.   60\.  180.]

```

**参考文献:**[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . degrees . html # numpy . degrees](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.degrees.html#numpy.degrees)
。