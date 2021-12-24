# Numpy recarray.repeat()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-repeat-function-python/](https://www.geeksforgeeks.org/numpy-recarray-repeat-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.repeat()`** 功能用于重复记录数组的元素。

> **语法:** `numpy.recarray.repeat(repeats, axis=None)` 
> 
> **参数:**
> **重复:**【int 或 int 数组】每个元素的重复次数。
> **轴:**【int 或 None】沿其重复值的轴。如果为“无”，则在重复之前先展平数组。
> 
> **返回:**【n 数组】输出数组，除了沿给定轴外，与记录数组形状相同。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.repeat() method 

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

# applying recarray.repeat methods
# to float record array along axis 1
out_arr = rec_arr.a.repeat(3, axis = 1)
print ("Output repeated float array along axis 1 : ", out_arr) 

# applying recarray.repeat methods
# to float record array along default axis 
out_arr = rec_arr.a.repeat(2)
print ("Output repeated float array along default axis : ", out_arr) 

# applying recarray.repeat methods
# to int record array along axis 0
out_arr = rec_arr.b.repeat(2, axis = 0)
print ("Output repeated int array along axis 0 : ", out_arr) 

# applying recarray.repeat methods
# to int record array along default
out_arr = rec_arr.b.repeat(2)
print ("Output repeated int array along default axis : ", out_arr)  
```

**Output:**

> 输入数组:[[( 5。, 2) ( 3., -4) ( 6.，9)】
> 【(9。, 1) ( 5., 4) (-12.，-7)]
> 记录数组的 float: [[ 5。3.6.】
> 【9。5.-12.]]
> 记录 int 的数组:[[ 2 -4 9]
> [ 1 4 -7]]
> 
> 沿轴 1 输出重复的浮点数组:[[ 5。5.5.3.3.3.6.6.6.】
> 【9。9.9.5.5.5.-12.-12.-12.]]
> 沿默认轴输出重复的浮点数组:[5]。5.3.3.6.6.9.9.5.5.-12.-12.】
> 沿 0 轴输出重复 int 数组:【[2-4 9]】
> 【2-4 9】
> 【1 4-7】
> 【1 4-7】】
> 沿默认轴输出重复 int 数组:【2 2-4-4 9 1 4-7-7】

**代码#2 :**

我们将`numpy.recarray.repeat()`应用于整个记录数组。

```
# Python program explaining
# numpy.recarray.repeat() method 

# importing numpy as geek
import numpy as geek

# creating input array with 2 different field 
in_arr = geek.array([[(5.0, 2), (3.0, 4), (6.0, -7)],
                     [(9.0, 1), (6.0, 4), (-2.0, -7)]],
                     dtype =[('a', float), ('b', int)])

print ("Input record array : ", in_arr)

# convert it to a record array, 
# using arr.view(np.recarray)
rec_arr = in_arr.view(geek.recarray)

# applying recarray.repeat methods to  record array
out_arr = rec_arr.repeat(3)

print ("Output repeated record array : ", out_arr)
```

**Output:**

> 输入记录数组:[[( 5。, 2) ( 3., 4) ( 6.，-7)]
> [( 9。, 1) ( 6., 4) (-2., -7)]]
> 
> 输出重复记录数组:
> [( 5。, 2) ( 5., 2) ( 5., 2) ( 3., 4) ( 3., 4) ( 3., 4) ( 6.，-7)
> ( 6。, -7) ( 6., -7) ( 9., 1) ( 9., 1) ( 9., 1) ( 6., 4) ( 6.，4)
> ( 6。, 4) (-2., -7) (-2., -7) (-2., -7)]