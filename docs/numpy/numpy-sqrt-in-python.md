# python 中的 numpy.sqrt()

> 原文:[https://www.geeksforgeeks.org/numpy-sqrt-in-python/](https://www.geeksforgeeks.org/numpy-sqrt-in-python/)

`numpy.sqrt(array[, out])`函数用于按元素确定数组的正平方根。

> **语法:** numpy.sqrt()
> 
> **参数:**
> **数组:**【array _ like】必须确定平方根的输入值。
> **out:**【n 数组，可选】放置结果的备用数组对象；如果提供，其形状必须与*或*相同。
> 
> **返回:**【ndarray】返回数组中数字的平方根。

**代码#1 :**

```py
# Python program explaining
# numpy.sqrt() method 

# importing numpy
import numpy as geek 

# applying sqrt() method on integer numbers 
arr1 = geek.sqrt([1, 4, 9, 16])
arr2 = geek.sqrt([6, 10, 18])

print("square-root of an array1  : ", arr1)
print("square-root of an array2  : ", arr2)
```

**Output:**

```py
square-root of an array1  :  [ 1\.  2\.  3\.  4.]
square-root of an array2  :  [ 2.44948974  3.16227766  4.24264069]

```

**代码#2 :**

```py
# Python program explaining
# numpy.sqrt() method 

# importing numpy
import numpy as geek 

# applying sqrt() method on complex numbers
arr = geek.sqrt([4, -1, -5 + 9J])

print("square-root of an array  : ", arr)
```

**Output:**

```py
square-root of an array  :  [ 2.00000000+0.j  0.00000000+1.j  1.62721083+2.76546833j]

```

**代码#3 :**

```py
# Python program explaining
# numpy.sqrt() method 

# importing numpy
import numpy as geek 

# applying sqrt() method on negative element of real numbers 
arr = geek.sqrt([-4, 5, -6])

print("square-root of an array  : ", arr)
```

**Output:**

```py
RuntimeWarning: invalid value encountered in sqrt
square-root of an array  :  [ nan  2.23606798  nan]

```