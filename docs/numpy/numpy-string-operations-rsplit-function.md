# numpy 字符串操作| rsplit()函数

> 原文:[https://www . geesforgeks . org/numpy-string-operations-rsplit-function/](https://www.geeksforgeeks.org/numpy-string-operations-rsplit-function/)

`numpy.core.defchararray.rsplit(arr, sep=None, maxsplit=None)`是 numpy 中做字符串运算的另一个函数。它返回字符串中的单词列表，使用 sep 作为 arr 中每个元素的分隔符字符串。`rsplit()`方法从右边开始将每个字符串数组元素拆分成一个列表，而`split()`方法从左边开始将每个字符串数组元素拆分成一个列表。

> **参数:**
> **arr :** 类似字符串或 unicode 的数组。输入数组。
> **sep :** 【字符串或 unicode，可选】指定拆分字符串时使用的分隔符。
> **max split:**【int，可选】要做多少个最大劈叉。
> 
> **返回:包含列表对象的输出数组。**

**代码#1 :**

```
# Python program explaining
# numpy.char.rsplit() method 

# importing numpy 
import numpy as geek

# input array  
in_arr = geek.array(['geeks for geeks'])
print ("Input array : ", in_arr) 

# output array 
out_arr = geek.char.rsplit(in_arr)
print ("Output splitted array: ", out_arr) 
```

**Output:**

```
Input array :  ['geeks for geeks']
Output splitted array:  [['geeks', 'for', 'geeks']]

```

**代码#2 :**

```
# Python program explaining
# numpy.char.rsplit() method 

# importing numpy 
import numpy as geek

# input array 
in_arr = geek.array(['Num-py', 'Py-th-on', 'Pan-das'])
print ("Input array : ", in_arr) 

# output array 
out_arr = geek.char.rsplit(in_arr, sep ='-')
print ("Output splitted array: ", out_arr) 
```

**Output:**

```
Input array :  ['Num-py' 'Py-th-on' 'Pan-das']
Output splitted array:  [['Num', 'py'] ['Py', 'th', 'on'] ['Pan', 'das']]

```

**代码#3 :**

```
# Python program explaining
# numpy.char.rsplit() method 

# importing numpy 
import numpy as geek

# input array 
in_arr = geek.array(['Num-py', 'Py-th-on', 'Pan-das'])
print ("Input array : ", in_arr) 

# output array when maximum splitting 
# of every array element is 1
out_arr = geek.char.rsplit(in_arr, sep ='-', maxsplit = 1)
print ("Output splitted array: ", out_arr) 
```

**Output:**

```
Input array :  ['Num-py' 'Py-th-on' 'Pan-das']
Output splitted array:  [['Num', 'py'] ['Py-th', 'on'] ['Pan', 'das']]

```