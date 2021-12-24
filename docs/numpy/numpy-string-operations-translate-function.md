# numpy 字符串操作| translate()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-translate-function/](https://www.geeksforgeeks.org/numpy-string-operations-translate-function/)

`numpy.core.defchararray.translate(arr, table, deletechars=None)`是 numpy 中做字符串运算的另一个函数。对于 arr 中的每个元素，它返回一个字符串的副本，其中出现在可选参数*中的所有字符都被删除，剩余的字符已经通过给定的转换表进行了映射。如果要翻译的值不止一个，则传递一个字典给 maketrans 函数来创建一个翻译表。*

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。输入数组。
> **表:**翻译映射指定执行翻译。
> **删除字符:**字符串类型，要删除的字符。
> 
> **返回:**【ndarray】带有翻译值的字符串或 unicode 输出数组。

**代码#1 :**

```py
# Python program explaining
# numpy.core.defchararray.translate() method 

# importing numpy 
import numpy as geek

# input array 
in_arr = geek.array(['Weeks', 'our', 'Weeks'])
print ("Input original array : ", in_arr) 

# creating dictionary for translation table 
trans_dict ={"W": "G", "o": "f", "u": "o"} 

# creating translation table from dictionary 
trans_table ="Wou".maketrans(trans_dict) 

out_arr = geek.core.defchararray.translate(in_arr, trans_table, deletechars ="None")
print ("Output translated array: ", out_arr) 
```

**Output:**

```py
Input original array :  ['Weeks' 'our' 'Weeks']
Output translated array:  ['Geeks' 'for' 'Geeks']

```