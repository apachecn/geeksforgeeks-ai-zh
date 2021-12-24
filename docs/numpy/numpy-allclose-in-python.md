# Python 中的 numpy.allclose()

> 原文:[https://www.geeksforgeeks.org/numpy-allclose-in-python/](https://www.geeksforgeeks.org/numpy-allclose-in-python/)

**`numpy.allclose()`** 函数用于查找两个数组在公差范围内是否元素相等。公差值是正数，通常是非常小的数字。将相对差值(rtol * abs(arr2))和绝对差值*叠加在一起*以对比 *arr1* 和 *arr2* 之间的绝对差值。如果任一数组包含一个或多个 nan，则返回 False。如果 INF 在两个数组中的位置相同，符号相同，则视为相等。

如果下面的等式在元素方面为真，那么 allclose 返回真。
`absolute(arr1 - arr2) <= (atol + rtol * absolute(arr2))`
As，上述方程在 arr1 和 arr2 中是不对称的，所以，allclose(arr1，arr2)在某些罕见的情况下可能与 allclose(arr2，arr1)不同。

> **语法:** numpy.allclose(arr1，arr2，rtol，环礁，equal_nan=False)
> 
> **参数:**
> **arr1 :** 【阵样】输入第 1 阵。
> **arr2 :** 【类阵】输入第二阵。
> **rtol :** 【浮动】相对公差参数。
> **环礁:**【浮动】绝对公差参数。
> **相等 _ nan:**【bool】是否将 NaN 的比较为相等。如果为真，arr1 中的 NaN 将被视为等于输出数组中 arr2 中的 NaN。
> 
> **返回:**【bool】如果两个数组在给定容差内相等，则返回 True，否则返回 False。

**代码#1 :**

```
# Python program explaining
# allclose() function

import numpy as geek

# input arrays
in_arr1 = geek.array([5e5, 1e-7, 4.000004e6])
print ("1st Input array : ", in_arr1) 

in_arr2 = geek.array([5.00001e5, 1e-7, 4e6])
print ("2nd Input array : ", in_arr2) 

# setting the absolute and relative tolerance
rtol = 1e-05
atol = 1e-08

res = geek.allclose(in_arr1, in_arr2, rtol, atol)
print ("Are the two arrays are equal within the tolerance: \t", res)
```

**Output:**

```
1st Input array :  [  5.00000000e+05   1.00000000e-07   4.00000400e+06]
2nd Input array :  [  5.00001000e+05   1.00000000e-07   4.00000000e+06]
Are the two arrays are equal within the tolerance:      True

```

**代码#2 :**

```
# Python program explaining
# allclose() function

import numpy as geek

# input arrays
in_arr1 = geek.array([5e5, 1e-7, 4.000004e6])
print ("1st Input array : ", in_arr1) 

in_arr2 = geek.array([5.00001e5, 1e-7, 4e6])
print ("2nd Input array : ", in_arr2) 

# setting the absolute and relative tolerance
rtol = 1e-06
atol = 1e-09

res = geek.allclose(in_arr1, in_arr2, rtol, atol)
print ("Are the two arrays are equal within the tolerance: \t", res)
```

**Output:**

```
1st Input array :  [5000000.0, 1e-07, 40000004.0]
2nd Input array :  [5000001.0, 1e-07, 40000000.0]
Are the two arrays are equal within the tolerance:      True

```

**代码#3 :**

```
# Python program explaining
# allclose() function

import numpy as geek

# input arrays
in_arr1 = geek.array([5e5, 1e-7, geek.nan])
print ("1st Input array : ", in_arr1) 

in_arr2 = geek.array([5e5, 1e-7, geek.nan])
print ("2nd Input array : ", in_arr2) 

# setting the absolute and relative tolerance
rtol = 1e-06
atol = 1e-09

res = geek.allclose(in_arr1, in_arr2, rtol, atol)
print ("Are the two arrays are equal within the tolerance: \t", res)
```

**Output:**

```
1st Input array :  [500000.0, 1e-07, nan]
2nd Input array :  [500000.0, 1e-07, nan]
Are the two arrays are equal within the tolerance:      False

```

**代码#4 :**

```
# Python program explaining
# allclose() function

import numpy as geek

# input arrays
in_arr1 = geek.array([5e5, 1e-7, geek.nan])
print ("1st Input array : ", in_arr1) 

in_arr2 = geek.array([5e5, 1e-7, geek.nan])
print ("2nd Input array : ", in_arr2) 

# setting the absolute and relative tolerance
rtol = 1e-06
atol = 1e-09

res = geek.allclose(in_arr1, in_arr2, rtol, atol, 
                                equal_nan = True)

print ("Are the two arrays are equal within the tolerance: \t", res)
```

**Output:**

```
1st Input array :  [500000.0, 1e-07, nan]
2nd Input array :  [500000.0, 1e-07, nan]
Are the two arrays are equal within the tolerance:      True

```