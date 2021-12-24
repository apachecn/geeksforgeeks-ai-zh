# numpy.isscalar()用 Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-isscalar-python/

**numpy.isscalar(num) :** 这是一个逻辑函数，如果输入 num 的类型是**标量**，则返回 true。

**参数:**

```
num : Input argument of any type and shape.
```

**返回:**

```
True, if input is scalar; else False

```

**代码 1:工作**

```
# Python program explaining
# isscalar() function
import numpy as np

in_array = [1, 3, 5, 4]
print ("Input array : ", in_array)

isscalar_values = np.isscalar(in_array)
print ("\nIs scalar : ", isscalar_values)

# input
print ("\nisscalar(7) : ", np.isscalar(7))

# list input 
print ("\nisscalar([7]) : ", np.isscalar([7]))
```

**输出:**

```
Input array :  [1, 3, 5, 4]

Is scalar :  False

isscalar(7) :  True

isscalar([7]) :  False

```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . isscalar . html](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.isscalar.html)
。