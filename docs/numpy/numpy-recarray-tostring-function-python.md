# Numpy recarray.tostring()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-recarray-tostring-function-python/](https://www.geeksforgeeks.org/numpy-recarray-tostring-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。

记录数组允许使用`arr.a and arr.b`作为数组成员访问字段。 **`numpy.recarray.tostring()`** 函数构造包含数组中原始数据字节的 Python 字节。

> **语法:** `numpy.recarray.tostring(order='C')`
> 
> **参数:**
> **顺序:** ['C '，' F '，无，可选]多维数组的数据顺序:C，Fortran，或与原始数组相同。
> 
> **返回:**【字节】显示记录数组原始数据副本的 Python 字节。

**代码#1 :**

```
# Python program explaining
# numpy.recarray.tostring() method 

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

# applying recarray.tostring methods
# to float record array in default order
out_arr = rec_arr.a.tostring()
print ("Output Python bytes of float record array in default order ", out_arr) 
print()

# applying recarray.tostring methods
# to float record array in fortan order
out_arr = rec_arr.a.tostring(order ='F')
print ("Output Python bytes of float record array in fortan order ", out_arr) 
print()

# applying recarray.tostring methods 
# to int record array in default order
out_arr = rec_arr.b.tostring()
print ("Output Python bytes of int record array in default order ", out_arr) 
print()

# applying recarray.tostring methods 
# to int record array in fortan order
out_arr = rec_arr.b.tostring(order ='F')
print ("Output Python bytes of int record array in fortan order ", out_arr) 
```

**Output:**

> 输入数组:[[( 5。, 2) ( 3., -4) ( 6.，9)】
> 【(9。, 1) ( 5., 4) (-12.，-7)]
> 记录数组的 float: [[ 5。3.6.】
> 【9。5.-12.]
> int 的记录数组:[[ 2 -4 9]
> [ 1 4 -7]]
> 以默认顺序 b '输出浮点记录数组的 Python 字节\ x00 \ x00 \ x00 \ x00 \ x00 \ x14 @ \ x00 \ x00 \ x00 \ x00 \ x00 \ x08 @ \ x00 \ x00 \ x00 \ x00 \ x00 \ x00 \ x18 @ \ x00 \ x00 \ x00 \ x00 \
> 
> 以 b '的顺序输出浮点记录数组的 Python 字节\ x00 \ x00 \ x00 \ x00 \ x00 \ x14 @ \ x00 \ x00 \ x00 \ x00 \ x00 “@ \ x00 \ x00 \ x00 \ x00 \ x08 @ \ x00 \ x00 \ x00 \ x00 \ x14 @ \ x00 \ x00 \ x00 \ x00 \ x00 \ x00 \ x00 \ x00 \ x18 @ \ x00 \ x00
> 
> 按默认顺序输出 int 记录数组的 Python 字节 b ' \ x02 \ x00 \ x00 \ x00 \ xfc \ xff \ xff \ xff \ t \ x00 \ x00 \ x00 \ x01 \ x00 \ x00 \ x04 \ x00 \ x00 \ x00 \ xf9 \ xff \ xff \ xff \ xff \ xff '
> 
> 按顺序 b '输出 int 记录数组的 Python 字节\ x02 \ x00 \ x00 \ x00 \ x01 \ x00 \ x00 \ x00 \ xfc \ xff \ xff \ xff \ x04 \ x00 \ x00 \ t \ x00 \ x00 \ x00 \ xf9 \ xff \ xff \ xff '

**代码#2 :**

我们将`numpy.recarray.tostring()`应用于整个记录数组。

```
# Python program explaining
# numpy.recarray.tostring() method 

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

# applying recarray.tostring methods to  
# record array in default order
out_arr = rec_arr.tostring()
print ("Output Python bytes of record array in default order ", out_arr) 
print()

# applying recarray.tostring methods to  
# record array in fortan order
out_arr = rec_arr.tostring(order ='F')
print ("Output Python bytes of record array in fortan order ", out_arr) 
```

**Output:**

> 输入数组:[( 5，2) ( 3，4) ( 6，-7)]
> [(9，1) ( 6，4) (-2，-7)]]
> 默认顺序 b 中记录数组 Python 字节的输出:\ 0x 00 \ 0x 00 \ 0x 00 \ x 00 \ x 00 \ x 00 \ x 14 @ \ x02 \ x 00 \ x 00 \ x 00 \ x 00 \ x 00 \ x 00 \ x 00 \ x 00 \ x 00 \ x 00 \ x 00 \ x 00 \ x 00 \ x 08 @ \ x4 \ x
> 
> Python 输出记录数组字节，位于 fortan order b ' \ 0x 00 \ 0x 00 \ x0 \ x 00 \ x14 @ \ x02 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 @ \ x01 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 08 @ \ x04 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ 0x 00 \ x 00 \ x 00 00 \ x 00 00 00 \ x 00 00