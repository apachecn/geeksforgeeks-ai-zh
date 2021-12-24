# Python 中的 numpy.sign()

> 原文:[https://www.geeksforgeeks.org/numpy-sign-in-python/](https://www.geeksforgeeks.org/numpy-sign-in-python/)

**numpy.sign(array [，out])** 函数用于按元素表示数字的符号。
对于整数输入，如果数组值大于 0 则返回 1，如果数组值小于 0 则返回-1，如果数组值为 0 则返回 0。

> **语法:** numpy.sign()
> 
> **参数:**
> **数组:**【array _ like】输入值。
> **出:**【n 数组，可选】输出数组放置有结果。
> 
> **返回:**【ndarray】返回数组的符号。如果一个数组是标量，那么数组的符号就是标量。

**代码 1 :**

```py
# Python Program illustrating
# numpy.sign() method

# importing numpy
import numpy as geek  

# input arrays    
array1 = [1, 0, -13]
array2 =  [-1, 0, 15]

# print the input arrays  
print ("input array1 : ", array1)
print ("input array2 : ", array2)

# determine the sign of integer numbers in an array  
print ("\nCheck sign of array1 : ", geek.sign(array1))
print ("\nCheck sign of array2 : ", geek.sign(array2)) 
```

**输出:**

```py
array1 :  [1, 0, -13]
array2 :  [-1, 0, 15]

Check sign of array1 :  [ 1  0 -1]

Check sign of array2 :  [-1  0  1]

```

**代码 2 :**

```py
# Python Program illustrating
# numpy.sign() method

# importing numpy  
import numpy as geek 

# determine the sign of complex number
print ("\n Check sign of complex input1 : ", geek.sign(7-3j))
print ("\n Check sign of complex input2 : ", geek.sign(-7 + 3j)) 
```

**输出:**

```py
 Check sign of complex input1 :  (1+0j)

 Check sign of complex input2 :  (-1+0j)

```