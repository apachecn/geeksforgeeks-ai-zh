# Numpy ufunc |通用功能

> 原文:[https://www . geeksforgeeks . org/numpy-ufunc-universal-functions/](https://www.geeksforgeeks.org/numpy-ufunc-universal-functions/)

**Numpy 中的泛函数**是简单的数学函数。这只是我们在 Numpy 库中赋予数学函数的一个术语。Numpy 提供各种通用功能，涵盖各种操作。
这些函数包括标准三角函数、算术运算函数、处理复数的函数、统计函数等。通用功能具有如下各种特性-

*   这些函数在**数组** (N 维数组)上运行，即 Numpy 的数组类。
*   它执行快速的按元素排列的数组操作。
*   它支持各种功能，如阵列广播，类型铸造等。
*   Numpy，universal functions 是属于 numpy.ufunc 类的对象。
*   Python 函数也可以使用 **frompyfunc** 库函数创建为通用函数。
*   当在数组上使用相应的算术运算符时，会自动调用一些**ufunc**。例如，当使用“+”运算符逐元素执行两个数组的加法时，则在内部调用 np.add()。

**Numpy 中的一些基本通用函数是-**

### 三角函数:

这些函数对弧度起作用，因此角度需要通过乘以π/180 转换成弧度。只有这样我们才能称之为三角函数。他们将数组作为输入参数。它包括的功能有-

| 功能 | 描述 |
| 唱歌，cos，晒黑 | 计算角度的正弦、余弦和正切值 |
| 阿尔辛，阿尔科斯，阿尔坦 | 计算反正弦、余弦和正切值 |
| 海波 | 计算给定直角三角形的斜边 |
| sinh，cosh，tanh | 计算双曲正弦、余弦和正切 |
| 亚契、亚契、亚契 | 计算反双曲正弦、余弦和正切 |
| deg2rad | 将度数转换成弧度 |
| 行 2 度 | 将弧度转换为度数 |

## 蟒蛇 3

```
# Python code to demonstrate trigonometric function
import numpy as np

# create an array of angles
angles = np.array([0, 30, 45, 60, 90, 180]) 

# conversion of degree into radians
# using deg2rad function
radians = np.deg2rad(angles)

# sine of angles
print('Sine of angles in the array:')
sine_value = np.sin(radians)
print(np.sin(radians))

# inverse sine of sine values
print('Inverse Sine of sine values:')
print(np.rad2deg(np.arcsin(sine_value)))

# hyperbolic sine of angles
print('Sine hyperbolic of angles in the array:')
sineh_value = np.sinh(radians)
print(np.sinh(radians))

# inverse sine hyperbolic 
print('Inverse Sine hyperbolic:')
print(np.sin(sineh_value)) 

# hypot function demonstration
base = 4
height = 3
print('hypotenuse of right triangle is:')
print(np.hypot(base, height))
```

**Output:** 

```
Sine of angles in the array:
[  0.00000000e+00   5.00000000e-01   7.07106781e-01   8.66025404e-01
   1.00000000e+00   1.22464680e-16]

Inverse Sine of sine values:
[  0.00000000e+00   3.00000000e+01   4.50000000e+01   6.00000000e+01
   9.00000000e+01   7.01670930e-15]

Sine hyperbolic of angles in the array:
[  0\.           0.54785347   0.86867096   1.24936705   2.3012989
  11.54873936]

Inverse Sine hyperbolic:
[ 0\.          0.52085606  0.76347126  0.94878485  0.74483916 -0.85086591]

hypotenuse of right triangle is:
5.0
```

### 统计功能:

这些函数用于计算数组元素的平均值、中值、方差和最小值。它包括像-
这样的功能

<figure class="table">

| 功能 | 描述 |
| on， amax | 返回数组或沿轴的最小值或最大值 |
| ptp | 返回数组或沿轴的值范围(最大值-最小值) |
| 百分位数(a，p，轴) | 计算数组或沿指定轴的 pth 百分比 |
| 中位数 | 计算沿指定轴的数据中值 |
| 意思是 | 沿指定轴计算数据平均值 |
| 标准 | 计算沿指定轴的数据标准偏差 |
| 定义变量 | 计算沿指定轴的数据方差 |
| 平均的 | 计算沿指定轴的数据平均值 |

</figure>

## 蟒蛇 3

```
# Python code demonstrate statistical function
import numpy as np

# construct a weight array
weight = np.array([50.7, 52.5, 50, 58, 55.63, 73.25, 49.5, 45])

# minimum and maximum 
print('Minimum and maximum weight of the students: ')
print(np.amin(weight), np.amax(weight))

# range of weight i.e. max weight-min weight
print('Range of the weight of the students: ')
print(np.ptp(weight))

# percentile
print('Weight below which 70 % student fall: ')
print(np.percentile(weight, 70))

# mean 
print('Mean weight of the students: ')
print(np.mean(weight))

# median 
print('Median weight of the students: ')
print(np.median(weight))

# standard deviation 
print('Standard deviation of weight of the students: ')
print(np.std(weight))

# variance 
print('Variance of weight of the students: ')
print(np.var(weight))

# average 
print('Average weight of the students: ')
print(np.average(weight))
```

**Output:** 

```
Minimum and maximum weight of the students: 
45.0 73.25

Range of the weight of the students: 
28.25

Weight below which 70 % student fall: 
55.317

Mean weight of the students: 
54.3225

Median weight of the students: 
51.6

Standard deviation of weight of the students: 
8.05277397857

Variance of weight of the students: 
64.84716875

Average weight of the students: 
54.3225
```

### 位旋转功能:

这些函数接受整数值作为输入参数，并对这些整数的二进制表示执行按位运算。它包括类似于-
功能

<figure class="table">

| 功能 | 描述 |
| 按位“与” | 对两个数组元素执行按位“与”运算 |
| 战斗或 | 对两个数组元素执行按位“或”运算 |
| 按位异或 | 对两个数组元素执行按位异或运算 |
| 转化的 | 对数组元素执行按位反转 |
| 左移 | 向左移动元素的位 |
| 右移 | 向左移动元素的位 |

</figure>

## 蟒蛇 3

```
# Python code to demonstrate bitwise-function
import numpy as np

# construct an array of even and odd numbers
even = np.array([0, 2, 4, 6, 8, 16, 32])
odd = np.array([1, 3, 5, 7, 9, 17, 33])

# bitwise_and
print('bitwise_and of two arrays: ')
print(np.bitwise_and(even, odd))

# bitwise_or
print('bitwise_or of two arrays: ')
print(np.bitwise_or(even, odd))

# bitwise_xor
print('bitwise_xor of two arrays: ')
print(np.bitwise_xor(even, odd))

# invert or not
print('inversion of even no. array: ')
print(np.invert(even))

# left_shift 
print('left_shift of even no. array: ')
print(np.left_shift(even, 1))

# right_shift 
print('right_shift of even no. array: ')
print(np.right_shift(even, 1))
```

**Output:** 

```
bitwise_and of two arrays: 
[ 0  2  4  6  8 16 32]

bitwise_or of two arrays: 
[ 1  3  5  7  9 17 33]

bitwise_xor of two arrays: 
[1 1 1 1 1 1 1]

inversion of even no. array: 
[ -1  -3  -5  -7  -9 -17 -33]

left_shift of even no. array: 
[ 0  4  8 12 16 32 64]

right_shift of even no. array: 
[ 0  1  2  3  4  8 16]
```