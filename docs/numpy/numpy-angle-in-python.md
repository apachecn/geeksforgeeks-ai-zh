# Python 中的 numpy.angle()

> 原文:[https://www.geeksforgeeks.org/numpy-angle-in-python/](https://www.geeksforgeeks.org/numpy-angle-in-python/)

**`numpy.angle()`** 功能是在我们想要计算复杂论证的角度时使用的。复数用**“x+yi”**表示，其中 x 和 y 是实数，`i= (-1)^1/2`。角度由公式`tan-1(x/y).`计算

> **语法:** numpy.angle(z，deg=0)
> 
> **参数:**
> **z:**【array _ like】复数或复数序列。
> **度:**【bool，可选】如果为真则返回角度，如果为假则返回弧度(默认)。
> 
> **返回:**
> **角度:**复平面上正实轴的逆时针角度，数据类型为 numpy.float64。

**代码#1:工作**

```
# Python program explaining
# numpy.angle() function
# when we want answer in radian

import numpy as geek
in_list =[2.0, 1.0j, 1 + 1j]

print ("Input  list : ", in_list)

out_angle = geek.angle(in_list) 
print ("output angle in radians : ", out_angle) 
```

**输出:**

```
Input  list :  [2.0, 1j, (1+1j)]
output angle in radians :  [ 0\.          1.57079633  0.78539816]

```

**代码#2:工作**

```
# Python program explaining
# numpy.angle() function
# when we want answer in degrees

import numpy as geek
in_list =[2.0, 1.0j, 1 + 1j]

print ("Input  list : ", in_list)

out_angle = geek.angle(in_list, deg = True) 
print ("output angle in degrees : ", out_angle) 
```

**输出:**

```
Input  list :  [2.0, 1j, (1+1j)]
output angle in degrees :  [  0\.  90\.  45.]

```