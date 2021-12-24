# Python 中的 numpy.hypot()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-hyp-python/

这个数学函数帮助用户计算直角三角形的斜边，给定它的边和垂线。按元素计算，结果相当于 *sqrt(x1**2 + x2**2)* 。
**语法:**

```py
numpy.exp2(arr1, arr2[, out]) = ufunc 'hypot') : 
```

**参数:**

```py
arr1, arr2  : *[array_like]* Legs(side and perpendicular) of triangle
out         : *[ndarray, optional]* Output array with result.

```

**返回:**

```py
An array having hypotenuse of the right triangle.

```

**代码#1:工作**

```py
# Python3 program explaining
# hypot() function

import numpy as np

leg1 = [12, 3, 4, 6]
print ("leg1 array : ", leg1)

leg2 = [5, 4, 3, 8]
print ("leg2 array : ", leg2)

result = np.hypot(leg1, leg2)
print("\nHypotenuse is as follows :")
print(result)
```

**输出:**

```py
leg1 array :  [12, 3, 4, 6]
leg2 array :  [5, 4, 3, 8]

Hypotenuse is as follows :
[ 13\.   5\.   5\.  10.]

```

**代码#2:使用 2D 阵**

```py
# Python3 program explaining
# hypot() function

import numpy as np

leg1 = np.random.rand(3, 4)
print ("leg1 array : \n", leg1)

leg2 = np.ones((3, 4))
print ("leg2 array : \n", leg2)

result = np.hypot(leg1, leg2)
print("\nHypotenuse is as follows :")
print(result)
```

**输出:**

```py
leg1 array : 
 [[ 0.57520509  0.12043366  0.50011671  0.13800957]
 [ 0.0528084   0.17827692  0.44236813  0.87758732]
 [ 0.94926413  0.47816742  0.46111934  0.63728903]]
leg2 array : 
 [[ 1\.  1\.  1\.  1.]
 [ 1\.  1\.  1\.  1.]
 [ 1\.  1\.  1\.  1.]]

Hypotenuse is as follows :
[[ 1.15362944  1.00722603  1.11808619  1.0094784 ]
 [ 1.00139339  1.01576703  1.09347591  1.33047342]
 [ 1.37880469  1.10844219  1.10119528  1.18580661]]
```

**代码 3:相当于 sqrt(x1**2 + x2**2)，元素方面。**

```py
# Python3 program explaining
# hypot() function

import numpy as np

leg1 = np.random.rand(3, 4)
print ("leg1 array : \n", leg1)

leg2 = np.ones((3, 4))
print ("leg2 array : \n", leg2)

result = np.sqrt((leg1 * leg1) + (leg2 * leg2))
print("\nHypotenuse is as follows :")
print(result)
```

**输出:**

```py
leg1 array : 
 [[ 0.7015073   0.89047987  0.1595603   0.27557254]
 [ 0.67249153  0.16430312  0.70137114  0.48763522]
 [ 0.68067777  0.52154819  0.04339669  0.2239366 ]]
leg2 array : 
 [[ 1\.  1\.  1\.  1.]
 [ 1\.  1\.  1\.  1.]
 [ 1\.  1\.  1\.  1.]]

Hypotenuse is as follows :
[[ 1.15362944  1.00722603  1.11808619  1.0094784 ]
 [ 1.00139339  1.01576703  1.09347591  1.33047342]
 [ 1.37880469  1.10844219  1.10119528  1.18580661]]
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-dev/reference/generated/numpy . hypot . html # numpy . hypot](https://docs.scipy.org/doc/numpy-dev/reference/generated/numpy.hypot.html#numpy.hypot)
。