# 结合一维和二维 NumPy 阵列

> 原文:[https://www . geeksforgeeks . org/combining-a-one-and-a-2d-numpy-array/](https://www.geeksforgeeks.org/combining-a-one-and-a-two-dimensional-numpy-array/)

有时我们需要组合一维和二维数组并显示它们的元素。Numpy 有一个名为 **numpy.nditer()，**的函数提供了这个功能。

> **语法:** numpy.nditer(op，flags=None，op_flags=None，op _ dtypes = None，order='K '，casting='safe '，op_axes=None，itershape=None，buffersize=0)

**例 1:**

## 蟒蛇 3

```
# importing Numpy package 
import numpy as np

num_1d = np.arange(5)
print("One dimensional array:")
print(num_1d)

num_2d = np.arange(10).reshape(2,5)
print("\nTwo dimensional array:")
print(num_2d)

# Combine 1-D and 2-D arrays and display 
# their elements using numpy.nditer() 
for a, b in np.nditer([num_1d, num_2d]):
    print("%d:%d" % (a, b),)
```

**输出:**

```
One dimensional array:
[0 1 2 3 4]

Two dimensional array:
[[0 1 2 3 4]
 [5 6 7 8 9]]
0:0
1:1
2:2
3:3
4:4
0:5
1:6
2:7
3:8
4:9

```

**例 2:**

## 蟒蛇 3

```
# importing Numpy package 
import numpy as np

num_1d = np.arange(7)
print("One dimensional array:")
print(num_1d)

num_2d = np.arange(21).reshape(3,7)
print("\nTwo dimensional array:")
print(num_2d)

# Combine 1-D and 2-D arrays and display 
# their elements using numpy.nditer() 
for a, b in np.nditer([num_1d, num_2d]):
    print("%d:%d" % (a, b),)
```

**输出:**

```
One dimensional array:
[0 1 2 3 4 5 6]

Two dimensional array:
[[ 0  1  2  3  4  5  6]
[ 7  8  9 10 11 12 13]
[14 15 16 17 18 19 20]]
0:0
1:1
2:2
3:3
4:4
5:5
6:6
0:7
1:8
2:9
3:10
4:11
5:12
6:13
0:14
1:15
2:16
3:17
4:18
5:19
6:20

```

**例 3:**

## 蟒蛇 3

```
# importing Numpy package 
import numpy as np

num_1d = np.arange(2)
print("One dimensional array:")
print(num_1d)

num_2d = np.arange(12).reshape(6,2)
print("\nTwo dimensional array:")
print(num_2d)

# Combine 1-D and 2-D arrays and display
# their elements using numpy.nditer() 
for a, b in np.nditer([num_1d, num_2d]):
    print("%d:%d" % (a, b),)
```

**输出:**

```
One dimensional array:
[0 1]

Two dimensional array:
[[ 0  1]
[ 2  3]
[ 4  5]
[ 6  7]
[ 8  9]
[10 11]]
0:0
1:1
0:2
1:3
0:4
1:5
0:6
1:7
0:8
1:9
0:10
1:11

```