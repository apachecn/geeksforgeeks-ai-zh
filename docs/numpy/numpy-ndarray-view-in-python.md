# python 中的 numpy . ndarray . view()

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-ndaarray-view-in-python/

**numpy.ndarray.view()** 有助于获得具有相同数据的数组的新视图。

> **语法:** ndarray.view(dtype=None，type=None)
> **参数:**
> **dtype :** 返回视图的数据类型描述符，例如 float32 或 int16。默认值“无”导致视图具有与 a 相同的数据类型。
> **类型:** Python 类型，可选的
> **返回:**数组或矩阵。

**代码#1:**

## 蟒蛇 3

```py
# Python program explaining 
# numpy.ndarray.view() function

import numpy as geek

a = geek.arange(10, dtype ='int16')

print("a is: \n", a)

# using view() method
v = a.view('int32')
print("\n After using view() with dtype = 'int32' a is : \n", a)

v += 1

# addition of 1 to each element of v
print("\n After using view() with dtype = 'int32' and adding 1 a is : \n", a)
```

**Output:** 

```py
a is: 
 [0 1 2 3 4 5 6 7 8 9]

 After using view() with dtype = 'int32' a is : 
 [0 1 2 3 4 5 6 7 8 9]

 After using view() with dtype = 'int32' and adding 1 a is : 
 [1 1 3 3 5 5 7 7 9 9]
```

**代码#2:**

## 蟒蛇 3

```py
# Python program explaining 
# numpy.ndarray.view() function

import numpy as geek

a = geek.arange(10, dtype ='int16')
print("a is:", a)

# Using view() method
v = a.view('int16')
print("\n After using view() with dtype = 'int16' a is :\n", a)

v += 1
# addition of 1 to each element of v
print("\n After using view() with dtype = 'int16' and adding 1 a is : \n", a)
```

**Output:** 

```py
a is: [0 1 2 3 4 5 6 7 8 9]

 After using view() with dtype = 'int16' a is :
 [0 1 2 3 4 5 6 7 8 9]

 After using view() with dtype = 'int16' and adding 1 a is : 
 [ 1  2  3  4  5  6  7  8  9 10]
```

**代码#3:**

## 蟒蛇 3

```py
# Python program explaining 
# numpy.ndarray.view() function

import numpy as geek

a = geek.arange(10, dtype ='int16')
print("a is: \n", a)

v = a.view('int8')
print("\n After using view() with dtype = 'int8' a is : \n", a)

v += 1
# addition of 1 to each element of v
print("\n After using view() with dtype = 'int8' and adding 1 a is : \n", a)
```