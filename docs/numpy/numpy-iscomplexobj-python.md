# num py . isccomplexibj()在 Python

中

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-isccomplexixobj-python/

**numpy . is complexobj(array):**这个逻辑函数有助于检查数组或复数数组的复杂类型。即使虚部等于零，它也被认为是一个复杂对象。

**参数:**

```
array    : [array_like]Input array or object whose elements, we need to test.
```

**返回:**

```
True, if the input array has a complex element; otherwise False 
```

**代码 1 :**

## 计算机编程语言

```
# Python program explaining
# iscomplexobj() function
import numpy as np

in_array = [1, 3, 5, 4]
print ("Input array : ", in_array)

output_value = np.iscomplexobj(in_array)
print ("\nIs complex : ", output_value)
```

**输出:**

```
Input array :  [1, 3, 5, 4]

Is complex :  False
```

**代码 2 :**

## 计算机编程语言

```
# Python Program illustrating
# numpy.iscomplexobj() method
import numpy as geek

# Returns True/False value for each element
a = geek.arange(20).reshape(5, 4)
print("Is complex : \n", geek.iscomplexobj(a))

# Returns True/False value as ans
# because we have mentioned dtpe in the beginning
b = geek.arange(20).reshape(5, 4).dtype = complex

print("\n",b)
print("\nIs complex : ", geek.iscomplexobj(b))

b = [[1j],
     [3]]
print("\nIs complex : \n", geek.iscomplexobj(b))
```

**输出:**

```
Is complex : 
 False

 class 'complex'

Is complex :  False

Is complex : 
 True
```

**参考资料:**
[【https://docs . scipy . org/doc/num py-1 . 13 . 0/reference/generated/num py . isccomplexibj . html # num py . isccomplexibj](https://docs.scipy.org/doc/numpy-1.13.0/reference/generated/numpy.iscomplexobj.html#numpy.iscomplexobj)