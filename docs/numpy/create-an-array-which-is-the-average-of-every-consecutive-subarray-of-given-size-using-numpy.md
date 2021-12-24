# 使用 NumPy

创建一个数组，该数组是给定大小的每个连续子数组的平均值

> 原文:[https://www . geeksforgeeks . org/create-array-这是给定大小的每个连续子阵列的平均值-使用-numpy/](https://www.geeksforgeeks.org/create-an-array-which-is-the-average-of-every-consecutive-subarray-of-given-size-using-numpy/)

在本文中，我们将看到创建元素数组的程序，其中每个元素都是给定的 n 大小的 [numpy 数组](https://www.geeksforgeeks.org/python-numpy/#:~:text=Array%20in%20Numpy%20is%20a,a%20tuple%20of%20positive%20integers.&text=An%20array%20class%20in%20Numpy,by%20using%20nested%20Python%20Lists.)的 k 大小的每个连续子数组的平均值，使得 k 是 n 的因子(即 n%k==0)。这个任务可以使用 [numpy.mean()](https://www.geeksforgeeks.org/numpy-mean-in-python/) 和[numpy . rescale()](https://www.geeksforgeeks.org/reshape-numpy-array/)功能一起完成。

> **语法:** numpy.mean(arr，axis = None)
> 
> **返回:**数组(如果轴为无，则为标量值)或沿指定轴有平均值的数组的算术平均值。
> 
> **语法:**numpy _ array . resform(shape)
> 
> **返回:**返回 numpy.ndarray

**示例:**

```py
Arr = [1,2,3,4,5,6
       7,8,9,10,11
       12,13,14,15,16] 
and K = 2 then 
Output is [ 1.5, 3.5, 5.5, 7.5, 
            9.5, 11.5, 13.5, 15.5].

Here, subarray of size k and there average are calculated as :

[1 2]    avg = ( 1 + 2 ) / 2 = 1.5  
[3 4]    avg = ( 3 + 4 ) / 2 = 3.5
[5 6]    avg = ( 5 + 6 ) / 2 = 5.5
[7 8]    avg = ( 7 + 8 ) / 2 = 7.5
[9 10]   avg = ( 9 + 10 ) / 2 = 9.5 
[11 12]  avg = ( 11 + 12 ) / 2 = 11.5 
[13 14]  avg = ( 13 + 14 ) / 2 = 13.5 
[15 16]  avg = ( 15 + 16 ) / 2 = 15.5

```

下面是实现:

## 蟒蛇 3

```py
# importing library
import numpy

# create numpy array
arr = numpy.array([1, 2, 3, 4, 5,
                   6, 7, 8, 9, 10,
                   11, 12, 13, 14,
                   15, 16])

# view array
print("Given Array:\n", arr)

# declare k
k = 2

# find the mean 
output = numpy.mean(arr.reshape(-1, k),
                    axis=1)

# view output
print("Output Array:\n", output)
```

**输出:**

```py
Given Array:
[ 1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16]
Output Array:
[ 1.5  3.5  5.5  7.5  9.5 11.5 13.5 15.5]

```