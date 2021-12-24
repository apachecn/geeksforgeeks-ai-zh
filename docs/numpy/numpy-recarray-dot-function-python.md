# Numpy recarray.dot()函数| Python

> 原文:[https://www . geesforgeks . org/numpy-recarray-dot-function-python/](https://www.geeksforgeeks.org/numpy-recarray-dot-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.dot()`** 函数返回两个记录数组的乘积。

> **语法:** `numpy.recarray.dot(arr, out=None)`
> 
> **参数:**
> **arr :** 秒录阵。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> 
> **Return :** 除非指定 out，否则将返回一个保存结果的新数组，在这种情况下，将返回该数组。
> 
> **代码#1 :**
> 
> ```py
> # Python program explaining
> # numpy.recarray.dot() method 
>   
> # importing numpy as geek
> import numpy as geek
>   
> # creating 2 input array with 2 different field 
> in_arr1 = geek.array([[(5.0, 2), (3.0, -4), (6.0, 9)],
>                      [(9.0, 1), (5.0, 4), (-12.0, -7)]],
>                      dtype =[('a', float), ('b', int)])
>   
> in_arr2 = geek.array([[(2.0, 1), (4.0, -3)],
>                      [(8.0, 3), (6.0, 5)],
>                      [(6.0, -5), (-5.0, 4)]],
>                      dtype =[('a', float), ('b', int)])
>   
> print ("1st Input array : ", in_arr1)
> print ("2nd Input array : ", in_arr2)
>   
> # convert it to a record array,
> # using arr.view(np.recarray)
> rec_arr1 = in_arr1.view(geek.recarray)
> print("1st Record array of float: ", rec_arr1.a)
> print("1st Record array of int: ", rec_arr1.b)
> rec_arr2 = in_arr2.view(geek.recarray)
> print("2nd Record array of float: ", rec_arr2.a)
> print("2nd Record array of int: ", rec_arr2.b)
>   
> # applying recarray.dot methods
> # between two float record array 
> out_arr1 = rec_arr1.a.dot( rec_arr2.a)
> print ("Output float array  : ", out_arr1) 
>   
> # applying recarray.dot methods
> # between two int record array 
> out_arr1 = rec_arr1.b.dot( rec_arr2.b)
> print ("Output int array  : ", out_arr1) 
> ```
> 
> **Output:**
> 
> ```py
> 1st Input array :  [[(  5.,  2) (  3., -4) (  6.,  9)]
>  [(  9.,  1) (  5.,  4) (-12., -7)]]
> 2nd Input array :  [[( 2.,  1) ( 4., -3)]
>  [( 8.,  3) ( 6.,  5)]
>  [( 6., -5) (-5.,  4)]]
> 1st Record array of float:  [[  5\.   3\.   6.]
>  [  9\.   5\. -12.]]
> 1st Record array of int:  [[ 2 -4  9]
>  [ 1  4 -7]]
> 2nd Record array of float:  [[ 2\.  4.]
>  [ 8\.  6.]
>  [ 6\. -5.]]
> 2nd Record array of int:  [[ 1 -3]
>  [ 3  5]
>  [-5  4]]
> Output float array  :  [[ 70\.   8.]
>  [-14\. 126.]]
> Output int array  :  [[-55  10]
>  [ 48 -11]]
> 
> ```