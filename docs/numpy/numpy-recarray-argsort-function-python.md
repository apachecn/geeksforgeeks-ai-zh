# Numpy recarray.argsort()函数| Python

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-reckler-argsort-function-python/

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.argsort()`** 函数返回对该数组进行排序的索引。

> **语法:** `numpy.recarray.argsort(arr, axis=-1, kind='quicksort', order=None)`
> 
> **参数:**
> **arr :** 输入记录数组。
> **轴:**【int 或 None】要排序的轴。如果为“无”，则数组在排序前被展平。默认值为-1，沿最后一个轴排序。
> **种类:** ['快速排序'，' mergesort '，' heap sort ']选择算法。默认值为“快速排序”。
> **顺序:**【字符串或字符串列表】当 arr 是定义了字段的数组时，此参数指定首先比较哪些字段，其次比较哪些字段等。
> 
> **返回:**【index _ Array，ndarray】沿指定轴排序的索引数组。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.argsort() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(5.0, 2), (3.0, -4), (6.0, 9)],
                     [(9.0, 1), (5.0, 4), (-12.0, -7)]],
                     dtype =[('a', float), ('b', int)])
print ("Input array : ", in_arr)

# convert it to a record array, 
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)
print("Record array of float: ", rec_arr.a)
print("Record array of int: ", rec_arr.b)

# applying recarray.argsort methods 
# to float record array along axis 1
out_arr = geek.recarray.argsort(rec_arr.a, axis = 1)
print ("Output sorted array indices along axis 1: ", out_arr) 

# applying recarray.argsort methods to
# int record array along axis 0
out_arr = geek.recarray.argsort(rec_arr.b, axis = 0)
print ("Output sorted array indices array along axis 0: ", out_arr) 
```

**Output:**

```
Input array :  [[(5.0, 2) (3.0, -4) (6.0, 9)]
 [(9.0, 1) (5.0, 4) (-12.0, -7)]]
Record array of float:  [[  5\.   3\.   6.]
 [  9\.   5\. -12.]]
Record array of int:  [[ 2 -4  9]
 [ 1  4 -7]]
Output sorted array indices along axis 1:  [[1 0 2]
 [2 1 0]]
Output sorted array indices array along axis 0:  [[1 0 1]
 [0 1 0]]

```

**代码#2 :**

我们将`numpy.recarray.argsort()`应用于整个记录数组。

```
# Python program explaining
# numpy.recarray.argsort() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(5.0, 2), (3.0, 4), (6.0, -7)],
                     [(9.0, 1), (6.0, 4), (-2.0, -7)]],
                     dtype =[('a', float), ('b', int)])
print ("Input array : ", in_arr)

# convert it to a record array, 
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)

# applying recarray.argsort methods to  record array
out_arr = geek.recarray.argsort(rec_arr, kind ='heapsort')

print ("Output array : ", out_arr)
```

**Output:**

```
Input array :  [[(5.0, 2) (3.0, 4) (6.0, -7)]
 [(9.0, 1) (6.0, 4) (-2.0, -7)]]
Output sorted array indices :  [[1 0 2]
 [2 1 0]]

```