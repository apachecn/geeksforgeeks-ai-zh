# Python |在 numpy 数组中添加行/列的方法

> 原文:[https://www . geesforgeks . org/python-numpy-array 中的行-列添加方式/](https://www.geeksforgeeks.org/python-ways-to-add-row-columns-in-numpy-array/)

给定 numpy 数组，任务是根据需求向 numpy 数组添加行/列。让我们看看这个问题的几个例子。
**方法#1:使用 np.hstack()方法**

## 蟒蛇 3

```
# Python code to demonstrate
# adding columns in numpy array

import numpy as np

ini_array = np.array([[1, 2, 3], [45, 4, 7], [9, 6, 10]])

# printing initial array
print("initial_array : ", str(ini_array));

# Array to be added as column
column_to_be_added = np.array([1, 2, 3])

# Adding column to numpy array
result = np.hstack((ini_array, np.atleast_2d(column_to_be_added).T))

# printing result
print ("resultant array", str(result))
```

**输出:**

```
initial_array :  [[ 1  2  3]
 [45  4  7]
 [ 9  6 10]]
resultant array [[ 1  2  3  1]
 [45  4  7  2]
 [ 9  6 10  3]]

```

**方法 2:使用 column_stack()方法**

## 蟒蛇 3

```
# python code to demonstrate
# adding columns in numpy array

import numpy as np

ini_array = np.array([[1, 2, 3], [45, 4, 7], [9, 6, 10]])

# printing initial array
print("initial_array : ", str(ini_array));

# Array to be added as column
column_to_be_added = np.array([1, 2, 3])

# Adding column to numpy array
result = np.column_stack((ini_array, column_to_be_added))

# printing result
print ("resultant array", str(result))
```

**输出:**

```
initial_array :  [[ 1  2  3]
 [45  4  7]
 [ 9  6 10]]
resultant array [[ 1  2  3  1]
 [45  4  7  2]
 [ 9  6 10  3]]

```

**方法#3:使用 np.vstack()方法**

## 蟒蛇 3

```
# python code to demonstrate
# adding rows in numpy array

import numpy as np

ini_array = np.array([[1, 2, 3], [45, 4, 7], [9, 6, 10]])

# printing initial array
print("initial_array : ", str(ini_array));

# Array to be added as row
row_to_be_added = np.array([1, 2, 3])

# Adding row to numpy array
result = np.vstack ((ini_array, row_to_be_added) )

# printing result
print ("resultant array", str(result))
```

**输出:**

```
initial_array :  [[ 1  2  3]
 [45  4  7]
 [ 9  6 10]]
resultant array [[ 1  2  3]
 [45  4  7]
 [ 9  6 10]
 [ 1  2  3]]

```

有时我们有一个空数组，需要在其中追加行。Numpy 提供了使用 **numpy.append()** 函数向空 Numpy 数组追加一行的功能。

```
Syntax : numpy.append(arr, values, axis=None)
```

**情况 1** :向空的二维数组中添加新行

## 蟒蛇 3

```
# importing Numpy package
import numpy as np  

# creating an empty 2d array of int type
empt_array = np.empty((0,2), int)
print("Empty array:")
print(empt_array)

# adding two new rows to empt_array
# using np.append()
empt_array = np.append(empt_array, np.array([[10,20]]), axis=0)
empt_array = np.append(empt_array, np.array([[40,50]]), axis=0)

print("\nNow array is:")
print(empt_array)
```

```
Empty array:
[]

Now array is:
[[10 20]
[40 50]]
```

**情况 2** :向空的三维数组中添加新行

## 蟒蛇 3

```
# importing Numpy package
import numpy as np  

# creating an empty 3d array of int type
empt_array = np.empty((0,3), int)
print("Empty array:")
print(empt_array)

# adding three new rows to empt_array
# using np.append()
empt_array = np.append(empt_array, np.array([[10,20,40]]), axis=0)
empt_array = np.append(empt_array, np.array([[40,50,55]]), axis=0)
empt_array = np.append(empt_array, np.array([[40,50,55]]), axis=0)

print("\nNow array is:")
print(empt_array)
```

```
Empty array:
[]

Now array is:
[[10 20 40]
 [40 50 55]
 [40 50 55]]
```

**情况 3** :向空的四维数组中添加新行

## 蟒蛇 3

```
# importing Numpy package
import numpy as np  

# creating an empty 4d array of int type
empt_array = np.empty((0,4), int)
print("Empty array:")
print(empt_array)

# adding four new rows to empt_array
# using np.append()
empt_array = np.append(empt_array, np.array([[100,200,400,888]]), axis=0)
empt_array = np.append(empt_array, np.array([[405,500,550,558]]), axis=0)
empt_array = np.append(empt_array, np.array([[404,505,555,145]]), axis=0)
empt_array = np.append(empt_array, np.array([[44,55,550,150]]), axis=0)

print("\nNow array is:")
print(empt_array)
```

```
Empty array:
[]

Now array is:
[[100 200 400 888]
 [405 500 550 558]
 [404 505 555 145]
 [ 44  55 550 150]]
```