# 使用 numpy

打印 nxn 棋盘图案的 Python 程序

> 原文:[https://www . geesforgeks . org/python-program-print-checkboard-pattern-nxn-using-numpy/](https://www.geeksforgeeks.org/python-program-print-checkerboard-pattern-nxn-using-numpy/)

给定 n，打印 n×n 矩阵的棋盘图案

**n = 8 的棋盘图案:**

它由 n * n 个正方形组成，白色为 0，黑色为 1。

我们可以使用嵌套循环的[和一些 if 条件来做同样的事情，但是使用 Python 的 numpy 库，我们可以导入一个二维矩阵，并使用切片来获得棋盘模式。
W2 将使用以下 python 函数打印图案:](https://www.geeksforgeeks.org/loops-in-python/)

```
[x = np.zeros((n, n), dtype=int)](https://www.geeksforgeeks.org/numpy-zeros-python/)
```

使用这个函数，我们使用 [numpy](https://www.geeksforgeeks.org/numpy-in-python-set-1-introduction/) 初始化一个所有索引都为 0 的二维矩阵

*   **x[1::2:::2]= 1**:从第一个索引行开始切片，直到 1+2+2…并从第 0 个到 0+2+2…用 1 填充所有列，以此类推。
*   **x[::2，1::2] = 1** :从第 0 行开始切片到 0+2+2…从 1 到 1+2+2+开始用 1 填充所有列…..

**NP . zero 的函数((n，n)，dtype=int) :** 通常，数组的元素最初是未知的，但其大小是已知的。因此，NumPy 提供了几个函数来创建带有初始占位符内容的数组。这使得增长阵列的必要性最小化，而增长阵列是一项昂贵的操作。使用 dtype 参数用 int 数据类型初始化所有值。
例如:NP . 0，NP . 1 等。

```
# Python program to print nXn
# checkerboard pattern using numpy

import numpy as np

# function to print Checkerboard pattern
def printcheckboard(n):

    print("Checkerboard pattern:")

    # create a n * n matrix
    x = np.zeros((n, n), dtype = int)

    # fill with 1 the alternate rows and columns
    x[1::2, ::2] = 1
    x[::2, 1::2] = 1

    # print the pattern
    for i in range(n):
        for j in range(n):
            print(x[i][j], end =" ") 
        print() 

# driver code
n = 8
printcheckboard(n)
```

输出:

```
Checkerboard pattern:
0 1 0 1 0 1 0 1 
1 0 1 0 1 0 1 0 
0 1 0 1 0 1 0 1 
1 0 1 0 1 0 1 0 
0 1 0 1 0 1 0 1 
1 0 1 0 1 0 1 0 
0 1 0 1 0 1 0 1 
1 0 1 0 1 0 1 0 

```

**基于棋盘格始终为偶数 nXn 即 n 为偶数**假设的改进源代码

```
# Python program to print nXn Assuming that n 
# is always even as a checkerboard was

import numpy as np
def printcheckboard(n):
    final = []
    for i in range(n):
        final.append(list(np.tile([0,1],int(n/2))) if i%2==0 else list(np.tile([1,0],int(n/2))))
    print(np.array(final))

# driver code
n = 8
printcheckboard(n)
```

输出:

```
Checkerboard pattern:
[[0 1 0 1 0 1 0 1]
 [1 0 1 0 1 0 1 0]
 [0 1 0 1 0 1 0 1]
 [1 0 1 0 1 0 1 0]
 [0 1 0 1 0 1 0 1]
 [1 0 1 0 1 0 1 0]
 [0 1 0 1 0 1 0 1]
 [1 0 1 0 1 0 1 0]]

```