# Python 中的 numpy.linalg.eig()方法

> 原文:[https://www . geesforgeks . org/numpy-linalg-EIG-method in-python/](https://www.geeksforgeeks.org/numpy-linalg-eig-method-in-python/)

在 NumPy 中，我们可以借助 **numpy.linalg.eig()计算给定方阵的特征值和右特征向量。**它将一个正方形数组作为参数，它将返回两个值，第一个是数组的特征值，第二个是给定正方形数组的右特征向量。

> **语法:** numpy.linalg.eig()
> 
> **参数:**一个方阵。
> 
> **Return:** 它会返回两个值第一个是特征值，第二个是特征向量。

**例 1:**

## 计算机编程语言

```py
import numpy as np

mat = np.mat("1 -2;1 3")

# Original matrix
print(mat)
print("")
evalue, evect = np.linalg.eig(mat)

# Eigenvalues of the said matrix"
print(evalue)
print("")

# Eigenvectors of the said matrix
print(evect)
```

**输出:**

```py
[[ 1 -2]
 [ 1  3]]

[2.+1.j 2.-1.j]

[[ 0.81649658+0.j          0.81649658-0.j        ]
 [-0.40824829-0.40824829j -0.40824829+0.40824829j]]

```

**例 2:**

## 计算机编程语言

```py
import numpy as np

mat = np.mat("1 2 3;1 3 4;3 2 1")

# Original matrix
print(mat)
print("")
evalue, evect = np.linalg.eig(mat)

# Eigenvalues of the said matrix"
print(evalue)
print("")

# Eigenvectors of the said matrix
print(evect)
```

**输出:**

```py
[[1 2 3]
 [1 3 4]
 [3 2 1]]

[ 6.70156212  0.29843788 -2\.        ]

[[-0.5113361  -0.42932334 -0.40482045]
 [-0.69070311  0.7945835  -0.52048344]
 [-0.5113361  -0.42932334  0.75180941]]

```