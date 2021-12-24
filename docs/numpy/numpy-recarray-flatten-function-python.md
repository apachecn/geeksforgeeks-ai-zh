# Numpy recarray . flat()函数| Python

> 原文:[https://www . geeksforgeeks . org/numpy-recarray-flat-function-python/](https://www.geeksforgeeks.org/numpy-recarray-flatten-function-python/)

在 numpy 中，数组可能具有包含字段的数据类型，类似于电子表格中的列。一个例子是`[(a, int), (b, float)]`，数组中的每个条目都是一对(int，float)。通常，这些属性是使用字典查找来访问的，例如`arr['a'] and arr['b']`。使用`arr.a and arr.b`，记录数组允许字段作为数组的成员被访问。

**`numpy.recarray.flatten()`** 函数返回一维的记录数组。

> **语法:** `numpy.recarray.flatten(order='C')`
> 
> **参数:**
> 
> **顺序:**[[[' C '，' F '，' A '，' K']，可选]
> “C”表示按行主(C 风格)顺序展平。
> “F”表示按列主(Fortran 风格)顺序展平。
> “A”的意思是，如果 A 在内存中是 Fortran 连续的，则按列主顺序展平，否则按行主顺序展平。
> “K”表示按照元素在内存中出现的顺序拉平。默认值为“C”。
> 
> **返回:**输入数组的副本，展平到一维。
> 
> **代码#1 :**
> 
> ```
> # Python program explaining
> # numpy.recarray.flatten() method 
>    
> # importing numpy as geek
> import numpy as geek
>    
> # creating input array with 2 different field 
> in_arr = geek.array([[(5.0, 2), (3.0, -4), (6.0, 9)],
>                      [(9.0, 1), (5.0, 4), (-12.0, -7)]],
>                      dtype =[('a', float), ('b', int)])
>   
> print ("Input array : ", in_arr)
>    
> # convert it to a record array,
> # using arr.view(np.recarray)
> rec_arr = in_arr.view(geek.recarray)
> print("Record array of float: ", rec_arr.a)
> print("Record array of int: ", rec_arr.b)
>    
> # applying recarray.flatten methods
> # to float record in Fortan order
> out_arr1 = rec_arr.a.flatten(order ='F')
> print ("Output float flattened array in Fortan order: ", out_arr1) 
>    
> # applying recarray.flatten methods 
> # to float record array in default order
> out_arr2 = rec_arr.a.flatten()
> print ("Output float flattenedarray in default order : ", out_arr2)
>   
> # applying recarray.flatten methods
> # to int record in 'A' order
> out_arr3 = rec_arr.b.flatten(order ='A')
> print ("Output int flattened array in A order: ", out_arr3) 
>    
> # applying recarray.flatten methods 
> # to float record array in 'K' order
> out_arr4 = rec_arr.b.flatten(order ='K')
> print ("Output intt flattened array in K order : ", out_arr4) 
> ```
> 
> **Output:**
> 
> ```
> Input array :  [[(  5.,  2) (  3., -4) (  6.,  9)]
>  [(  9.,  1) (  5.,  4) (-12., -7)]]
> Record array of float:  [[  5\.   3\.   6.]
>  [  9\.   5\. -12.]]
> Record array of int:  [[ 2 -4  9]
>  [ 1  4 -7]]
> Output float flattened array in Fortan order:  [  5\.   9\.   3\.   5\.   6\. -12.]
> Output float flattenedarray in default order :  [  5\.   3\.   6\.   9\.   5\. -12.]
> Output int flattened array in A order:  [ 2 -4  9  1  4 -7]
> Output intt flattened array in K order :  [ 2 -4  9  1  4 -7]
> 
> ```