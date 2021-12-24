# Python 中的 numpy.unwrap()

> 原文:[https://www.geeksforgeeks.org/numpy-unwrap-in-python/](https://www.geeksforgeeks.org/numpy-unwrap-in-python/)

**numpy.unwrap(p，折扣=3.141592653589793，axis=-1)** 功能通过将*增量*更改为 2*pi 补码的值来帮助用户打开给定数组。它通过沿给定轴将大于折扣的绝对跳跃改变为它们的 2 *π补码来展开弧度相位 *p* 。结果是一个展开的数组。

> **参数:**
> **p** : *【阵象】*输入阵
> **折扣** : *【浮动，可选】*值之间最大不连续，默认为 pi
> **轴**:*【int，可选】*轴打开将沿其操作，默认为最后一个轴
> **返回:**【ndarray】输出阵

**注:**如果 p 中的不连续性小于*π*，但大于折扣，则不进行展开，因为取 2 *π补码只会使不连续性变大。
**代码#1:默认值工作**

## 蟒蛇 3

```
import numpy as np

l1 =[1, 2, 3, 4, 5]
print("Result 1: ", np.unwrap(l1))

l2 =[0, 0.78, 5.49, 6.28]
print("Result 2: ", np.unwrap(l2))
```

**输出:**

```
Result 1: array([1., 2., 3., 4., 5.])
Result 2: array([ 0.,  0.78, -0.79318531, -0.00318531])
```

在 l2 中，折扣> 2*pi(介于 0.78 和 5.49 之间)，因此数组值会发生变化。
**代码#2:自定义值工作**

## 蟒蛇 3

```
import numpy as np

l1 =[5, 7, 10, 14, 19, 25, 32]
print("Result 1: ", np.unwrap(l1, discount = 4))

l2 =[0, 1.34237486723, 4.3453455, 8.134654756, 9.3465456542]
print("Result 2: ", np.unwrap(l2, discount = 3.1))
```

**输出:**

> 结果 1: [ 5。, 7., 10.，7.71681469，6.43362939，6.15044408，6.86725877]
> 结果 2: [0。, 1.34237487, 4.3453455, 1.85146945, 3.06336035]

**参考文献:**[https://docs . scipy . org/doc/numpy-1 . 15 . 1/参考/生成/numpy.unwrap.html](https://docs.scipy.org/doc/numpy-1.15.1/reference/generated/numpy.unwrap.html)