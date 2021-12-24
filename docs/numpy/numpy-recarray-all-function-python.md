# Numpy recarray.all()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-all-function-python/](https://www.geeksforgeeks.org/numpy-recarray-all-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。
记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.all()`** 如果记录数组中的所有元素都评估为真，则函数返回真。

> **语法:** `numpy.recarray.all(axis=None, out=None, keepdims=False)`
> 
> **参数:**
> **轴:**【无或整数或整数元组，可选】执行逻辑与归约的一个或多个轴。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **保持尺寸:**【布尔，可选】如果设置为真，则缩小的轴作为尺寸为 1 的尺寸留在结果中。使用此选项，结果将根据输入数组正确广播。
> 如果传递了默认值，那么 keepdims 将不会传递给 ndarray 的所有方法子类，但是任何非默认值都将传递。如果子类 sum 方法不实现 keepdims，将引发任何异常。
> 
> **返回:**【ndarray，bool】如果所有元素都计算为真，则返回真。

**代码#1 :**

```py
# Python program explaining
# numpy.recarray.all() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([(5.0, 2), (3.0, 4)],
         dtype =[('a', float), ('b', int)])
print ("Input array : ", in_arr)

# convert it to a record array, using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of float: ", rec_arr.a)
print("Record array of int: ", rec_arr.b)

# applying recarray.all methods to float record array
out_arr = geek.recarray.all(rec_arr.a)
print ("Output array: ", out_arr) 

# applying recarray.all methods to int record array
out_arr = geek.recarray.all(rec_arr.b)
print ("Output array: ", out_arr) 
```

**Output:**

```py
Input array :  [(5.0, 2) (3.0, 4)]
Record array of float:  [ 5\.  3.]
Record array of int:  [2 4]
Output array:  True
Output array:  True

```

**代码#2 :**

如果我们将`numpy.recarray.all()`应用于整个记录数组，那么它将给出`Type error`，因为数组是灵活的或混合类型的。

```py
# Python program explaining
# numpy.recarray.all() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([(5.0, 2), (3.0, 4)],
         dtype =[('a', float), ('b', int)])
print ("Input array : ", in_arr) 

# convert it to a record array, using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array ", rec_arr)

# applying recarray.all methods to  record array
out_arr = geek.recarray.all(rec_arr)
print ("Output array: ", out_arr)  
```

**Output:**

```py
TypeError: cannot perform reduce with flexible type

```