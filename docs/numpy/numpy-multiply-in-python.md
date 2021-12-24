# Python 中的 numpy.multiply()

> 原文:[https://www.geeksforgeeks.org/numpy-multiply-in-python/](https://www.geeksforgeeks.org/numpy-multiply-in-python/)

**`numpy.multiply()`** 函数是在我们要计算两个数组的乘法时使用的。它按元素返回 arr1 和 arr2 的乘积。

> **语法:** numpy.multiply(arr1，arr2，/，out=None，*，其中=True，casting='same_kind '，order='K '，dtype=None，subok=True[，signature，extobj]，ufunc 'multiply ')
> 
> **参数:**
> **arr 1:**【array _ like 或标量】第一输入数组。
> **arr2:** 【类数组或标量】第二输入数组。
> **dtype:** 返回数组的类型。默认情况下，使用 arr 的*数据类型*。
> **out:**【n 数组，可选】存储结果的位置。
> - >如果提供，它必须具有输入广播到的形状。
> - >如果未提供或无，则返回新分配的阵列。
> **其中:**【array _ like，可选】值为 True 表示计算该位置的 ufunc，值为 False 表示将该值单独留在输出中。
> ****kwargs:** 允许将关键字可变长度的参数传递给函数。当我们想要处理函数中的命名参数时使用。
> 
> **返回:**【数组或标量】arr1 和 arr2 的乘积，元素方式。

**示例#1 :**

```
# Python program explaining
# numpy.multiply() function

import numpy as geek
in_num1 = 4
in_num2 = 6

print ("1st Input  number : ", in_num1)
print ("2nd Input  number : ", in_num2)

out_num = geek.multiply(in_num1, in_num2) 
print ("output number : ", out_num) 
```

**Output :**

```
1st Input number :  4
2nd Input number :  6
output number :  24

```

**示例#2 :**
下面的代码也被称为哈达玛乘积，它只不过是两个矩阵的元素乘积。对于对机器学习或统计感兴趣的人来说，它是最常用的产品。

```
# Python program explaining
# numpy.multiply() function

import numpy as geek

in_arr1 = geek.array([[2, -7, 5], [-6, 2, 0]])
in_arr2 = geek.array([[0, -7, 8], [5, -2, 9]])

print ("1st Input array : ", in_arr1)
print ("2nd Input array : ", in_arr2)

out_arr = geek.multiply(in_arr1, in_arr2) 
print ("Resultant output array: ", out_arr) 
```

**Output :**

```
1st Input array :  [[ 2 -7  5]
 [-6  2  0]]
2nd Input array :  [[ 0 -7  8]
 [ 5 -2  9]]
Resultant output array:  [[  0  49  40]
 [-30  -4   0]]

```

另一个找到相同的方法是

```
import numpy as geek
in_arr1=geek.matrix([[2, -7, 5], [-6, 2, 0]])
in_arr2 = geek.matrix([[0, -7, 8], [5, -2, 9]])

print ("1st Input array : ", in_arr1)
print ("2nd Input array : ", in_arr2)

out_arr=geek.array(in_arr1)*geek.array(in_arr2)
print ("Resultant output array: ", out_arr)
```

**输出:**

```
1st Input array :  [[ 2 -7  5]
 [-6  2  0]]
2nd Input array :  [[ 0 -7  8]
 [ 5 -2  9]]
Resultant output array:  [[  0  49  40]
 [-30  -4   0]]

```