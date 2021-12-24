# 求一个 NumPy 数组元素的和与积

> 原文:[https://www . geeksforgeeks . org/find-a-numpy-array-elements 之和与乘积/](https://www.geeksforgeeks.org/find-the-sum-and-the-product-of-a-numpy-array-elements/)

在本文中，让我们讨论如何找到 NumPy 数组的和与积。

### NumPy 数组的和

NumPy 数组元素的总和可以通过以下方式实现

**方法#1:使用** [**numpy.sum()**](https://www.geeksforgeeks.org/numpy-sum-in-python/)

> **语法:** numpy.sum(array_name，axis=None，dtype=None，out=None，keepdims= <无值>，initial= <无值>，其中= <无值>

**示例:**

## 蟒蛇 3

```py
# importing numpy
import numpy as np

def main():

    # initialising array
    print('Initialised array')
    gfg = np.array([[1, 2, 3], [4, 5, 6]])
    print(gfg)

    # sum along row
    print(np.sum(gfg, axis=1))

    # sum along column
    print(np.sum(gfg, axis=0))

    # sum of entire array
    print(np.sum(gfg))

    # use of out
    # initialise a array with same dimensions
    # of expected output to use OUT parameter
    b = np.array([0])  # np.int32)#.shape = 1
    print(np.sum(gfg, axis=1, out=b))

    # the output is stored in b
    print(b)

    # use of keepdim
    print('with axis parameter')

    # output array's dimension is same as specified
    # by the axis
    print(np.sum(gfg, axis=0, keepdims=True))

    # output consist of 3 columns
    print(np.sum(gfg, axis=1, keepdims=True))

    # output consist of 2 rows
    print('without axis parameter')
    print(np.sum(gfg, keepdims=True))

    # we added 100 to the actual result
    print('using initial parameter in sum function')
    print(np.sum(gfg, initial=100))

    # False allowed to skip sum operation on column 1 and 2
    # that's why output is 0 for them
    print('using where parameter ')
    print(np.sum(gfg, axis=0, where=[True, False, False]))

if __name__ == "__main__":
    main()
```

**输出:**

```py
Initialised array
[[1 2 3]
 [4 5 6]]
[ 6 15]
[5 7 9]
21
[21]
[21]
with axis parameter
[[5 7 9]]
[[ 6]
 [15]]
without axis parameter
[[21]]
using initial parameter in sum function
121
using where parameter 
[5 0 0]
```

**注意:**对由非数字(NaNs)元素组成的数组元素使用 numpy.sum 会产生错误，为了避免这种情况，我们使用 [numpy。 **nansum()**](https://www.geeksforgeeks.org/numpy-nansum-in-python/) 参数与前者相似，只是后者不支持*，其中*和*为初始值。*

**方法 2:使用**[**numpy . cumsum()**](https://www.geeksforgeeks.org/numpy-cumsum-in-python/)

返回给定数组中元素的累积和。

> **语法:** numpy.cumsum(array_name，axis=None，dtype=None，out=None)

**示例:**

## 蟒蛇 3

```py
# importing numpy
import numpy as np

def main():

    # initialising array
    print('Initialised array')
    gfg = np.array([[1, 2, 3], [4, 5, 6]])

    print('original array')
    print(gfg)

    # cumulative sum of the array
    print(np.cumsum(gfg))

    # cumulative sum of the array along
    # axis 1
    print(np.cumsum(gfg, axis=1))

    # initialising a 2x3 shape array
    b = np.array([[None, None, None], [None, None, None]])

    # finding cumsum and storing it in array
    np.cumsum(gfg, axis=1, out=b)

    # printing resultant array
    print(b)

if __name__ == "__main__":
    main()
```

**输出:**

```py
Initialised array
original array
[[1 2 3]
 [4 5 6]]
[ 1  3  6 10 15 21]
[[ 1  3  6]
 [ 4  9 15]]
[[1 3 6]
 [4 9 15]]
```

### NumPy 数组的乘积

NumPy 阵列的产品可以通过以下方式实现

**方法#1:使用** [**numpy.prod()**](https://www.geeksforgeeks.org/numpy-prod-python/)

> **语法:** numpy。 **prod** (array_name，axis=None，dtype=None，out=None，keepdims= <无值>，初始值= <无值>，其中= <无值>

**示例:**

## 蟒蛇 3

```py
# importing numpy
import numpy as np

def main():

    # initialising array
    print('Initialised array')
    gfg = np.array([[1, 2, 3], [4, 5, 6]])
    print(gfg)

    # product along row
    print(np.prod(gfg, axis=1))

    # product along column
    print(np.prod(gfg, axis=0))

    # sum of entire array
    print(np.prod(gfg))

    # use of out
    # initialise a array with same dimensions
    # of expected output to use OUT parameter
    b = np.array([0])  # np.int32)#.shape = 1
    print(np.prod(gfg, axis=1, out=b))

    # the output is stored in b
    print(b)

    # use of keepdim
    print('with axis parameter')

    # output array's dimension is same as specified
    # by the axis
    print(np.prod(gfg, axis=0, keepdims=True))

    # output consist of 3 columns
    print(np.prod(gfg, axis=1, keepdims=True))

    # output consist of 2 rows
    print('without axis parameter')
    print(np.prod(gfg, keepdims=True))

    # we initialise product to a factor of 10
    # instead of 1
    print('using initial parameter in sum function')
    print(np.prod(gfg, initial=10))

    # False allowed to skip sum operation on column 1 and 2
    # that's why output is 1 which is default initial value
    print('using where parameter ')
    print(np.prod(gfg, axis=0, where=[True, False, False]))

if __name__ == "__main__":
    main()
```

**输出:**

```py
Initialised array
[[1 2 3]
 [4 5 6]]
[  6 120]
[ 4 10 18]
720
[720]
[720]
with axis parameter
[[ 4 10 18]]
[[  6]
 [120]]
without axis parameter
[[720]]
using initial parameter in sum function
7200
using where parameter 
[4 1 1]
```

**方法 2:使用**[**numpy . cumpd()**](https://www.geeksforgeeks.org/numpy-cumprod-in-python/)

返回数组的累积乘积。

> **语法:** numpy.cumsum(array_name，axis=None，dtype=None，out = None)axis =[整数，可选]

## 蟒蛇 3

```py
# importing numpy
import numpy as np

def main():

    # initialising array
    print('Initialised array')
    gfg = np.array([[1, 2, 3], [4, 5, 6]])
    print('original array')
    print(gfg)

    # cumulative product of the array
    print(np.cumprod(gfg))

    # cumulative product of the array along
    # axis 1
    print(np.cumprod(gfg, axis=1))

    # initialising a 2x3 shape array
    b = np.array([[None, None, None], [None, None, None]])

    # finding cumprod and storing it in array
    np.cumprod(gfg, axis=1, out=b)

    # printing resultant array
    print(b)

if __name__ == "__main__":
    main()
```

**输出:**

```py
Initialised array
original array
[[1 2 3]
 [4 5 6]]
[  1   2   6  24 120 720]
[[  1   2   6]
 [  4  20 120]]
[[1 2 6]
 [4 20 120]]
```