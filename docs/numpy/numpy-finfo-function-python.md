# numpy.finfo()函数–Python

> 原文:[https://www.geeksforgeeks.org/numpy-finfo-function-python/](https://www.geeksforgeeks.org/numpy-finfo-function-python/)

**`numpy.finfo()`** 功能显示浮点类型的机器限制。

> **语法:**num py . finfo(dttype)
> 
> **参数:**
> **数据类型:**【浮点、数据类型或实例】获取信息的浮点数据类型的种类。
> **返回:**浮点类型的机器参数。

**代码#1 :**

```
# Python program explaining
# numpy.finfo() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.finfo(geek.float32)

print (gfg)
```

**输出:**

```
Machine parameters for float32
---------------------------------------------------------------
precision =   6   resolution = 1.0000000e-06
machep =    -23   eps =        1.1920929e-07
negep =     -24   epsneg =     5.9604645e-08
minexp =   -126   tiny =       1.1754944e-38
maxexp =    128   max =        3.4028235e+38
nexp =        8   min =        -max
---------------------------------------------------------------

```

**代码#2 :**

```
# Python program explaining
# numpy.finfo() function

# importing numpy as geek 
import numpy as geek 

gfg = geek.finfo(geek.float64)

print (gfg)
```

**输出:**

```
Machine parameters for float64
---------------------------------------------------------------
precision =  15   resolution = 1.0000000000000001e-15
machep =    -52   eps =        2.2204460492503131e-16
negep =     -53   epsneg =     1.1102230246251565e-16
minexp =  -1022   tiny =       2.2250738585072014e-308
maxexp =   1024   max =        1.7976931348623157e+308
nexp =       11   min =        -max
---------------------------------------------------------------

```