# numpy.isrealobj()在 Python 中

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-isrealobj-python/

**numpy . isralobj(array):**这个逻辑函数有助于检查数组是否没有复数类型或者数组是否有复数。即使虚部等于零，也不认为是实物体。

**参数:**

```py
array    : [array_like]Input array or object whose elements, we need to test.

```

**返回:**

```py
True, if the input array hasn't any complex element; otherwise False 

```

**代码 1 :**

```py
# Python program explaining
# isrealobj() function
import numpy as np

in_array = [1, 3, 5, 4]
print ("Input array : ", in_array)

output_value = np.isrealobj(in_array)
print ("\nIs real : ", output_value)
```

**输出:**

```py
Input array :  [1, 3, 5, 4]

Is real :  True

```

**代码 2 :**

```py
# Python Program illustrating
# numpy.isrealobj() method   
import numpy as geek 

# Returns True/False value for each element 
a = geek.arange(20).reshape(5, 4)
print("Is real : ", geek.isrealobj(a))

# Returns True/False value as ans 
# because we have mentioned dtpe in the beginning
b = geek.arange(20).reshape(5, 4).dtype = complex

print("\n",b)
print("\nIs real : ", geek.isrealobj(b))

b = [[1j], 
     [3]]
print("\nIs real : ", geek.isrealobj(b))
```

**输出:**

```py
Is real :  True

 class 'complex'

Is real :  True

Is real :  False
```

**参考文献:**
[https://docs . scipy . org/doc/numpy-1 . 13 . 0/reference/generated/numpy . isralobj . html # numpy . isralobj](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.isrealobj.html#numpy.isrealobj)
。