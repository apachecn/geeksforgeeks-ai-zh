# numpy.arctan2()在 Python

中

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-arctan 2-python/

**numpy.arctan2()** 方法通过正确选择象限来计算 arr1/arr2 的元素弧切线。选择象限，使得 *arctan2(x1，x2)* 是以弧度为单位的有符号角度，该角度介于终止于原点并穿过点(1，0)的光线和终止于原点并穿过点(x2，x1)的光线之间。

> **语法:** numpy.arctan2(arr1，arr2，casting = 'same_kind '，order = 'K '，dtype = None，ufunc 'arctan')
> **参数:**
> **arr 1:***【array _ like】*实值；y 坐标
> **arr 2:***【array _ like】*实值；x 坐标。它必须与 y 坐标的形状相匹配。
> **out:***【n array，array _ like[OPTIONAL]】*与 x 形状相同的数组.
> **其中:***【array _ like，OPTIONAL】*True 值表示计算该位置的通用函数(ufunc)，False 值表示将该值单独留在输出中。
> **注:**
> 2pi 弧度= 360 度
> 惯例是返回实部位于[-pi/2，pi/2]的角度 z。
> **返回:**arr 1/arr 2 的元素方向反正切。值在封闭区间[-pi / 2，pi / 2]内。

**代码#1:工作**

## 蟒蛇 3

```
# Python3 program explaining
# arctan2() function

import numpy as np

arr1 = [-1, +1, +1, -1]
arr2 = [-1, -1, +1, +1]

ans = np.arctan2(arr2, arr1) * 180 / np.pi

print ("x-coordinates : ", arr1)
print ("y-coordinates : ", arr2)

print ("\narctan2 values : \n", ans)
```

**输出:**

```
x-coordinates :  [-1, 1, 1, -1]
y-coordinates :  [-1, -1, 1, 1]

arctan2 values : 
 [-135\.  -45\.   45\.  135.]
```

**代码#2:工作**

## 蟒蛇 3

```
# Python3 program showing
# of arctan2() function

import numpy as np

a = np.arctan2([0., 0., np.inf], [+0., -0., np.inf])

b = np.arctan2([1., -1.], [0., 0.])

print ("a : ", a)

print ("b : ", b)
```

**输出:**

```
a :  [ 0\.          3.14159265  0.78539816]
b :  [ 1.57079633 -1.57079633]
```

**参考资料:**
[https://docs . scipy . org/doc/num py-1 . 13 . 0/reference/generad/num py . arctan 2 . html # num py . arctan 2](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.arctan2.html#numpy.arctan2)
。