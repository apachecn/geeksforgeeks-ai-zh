# Python | numpy.cov()函数

> 原文:[https://www.geeksforgeeks.org/python-numpy-cov-function/](https://www.geeksforgeeks.org/python-numpy-cov-function/)

协方差提供了两个变量或多组变量之间相关强度的度量。协方差矩阵元素 C <sub>ij</sub> 是 xi 和 xj 的协方差。元素 Cii 是 xi 的方差。

*   如果 COV(xi，xj) = 0，那么变量是不相关的
*   如果 COV(xi，xj) > 0，则变量正相关
*   如果 COV(xi，XJ)> 0，则变量负相关

> **语法:** numpy.cov(m，y=None，rowvar=True，bias=False，ddof=None，fw thres = None，aw rights = None)
> **参数:**
> **m:**【array _ like】A 1D 或 2D 变量。变量是列
> **y:**【array _ like】它与 m 的形式相同。
> **rowvar:**【bool，可选】如果 row var 为 True(默认)，那么每一行代表一个变量，在列中带有观察值。否则，关系转置:
> **偏差:**默认归一化为假。如果偏差为真，则将数据点归一化。
> **ddof :** 如果不是“无”，将覆盖偏差隐含的默认值。请注意，即使同时指定了 fweights 和 aweights，ddof=1 也将返回无偏估计。
> **fw weight:**fw weight 是一维整数频率权重数组
> **aw weight:**aw weight 是一维观测向量权重数组。
> **返回:**返回数组协方差矩阵

**示例#1:**

## 蟒蛇 3

```
# Python code to demonstrate the
# use of numpy.cov
import numpy as np

x = np.array([[0, 3, 4], [1, 2, 4], [3, 4, 5]])

print("Shape of array:\n", np.shape(x))

print("Covariance matrix of x:\n", np.cov(x))
```

**输出:**

```
Shape of array:
 (3, 3)
Covariance matrix of x:
 [[ 4.33333333  2.83333333  2\.        ]
 [ 2.83333333  2.33333333  1.5       ]
 [ 2\.          1.5         1\.        ]]
```

**例 2:**

## 蟒蛇 3

```
# Python code to demonstrate the
# use of numpy.cov
import numpy as np

x = [1.23, 2.12, 3.34, 4.5]

y = [2.56, 2.89, 3.76, 3.95]

# find out covariance with respect  columns
cov_mat = np.stack((x, y), axis = 0)

print(np.cov(cov_mat))
```

**Output:** 

```
[[ 2.03629167  0.9313    ]
 [ 0.9313      0.4498    ]]
```

**示例#3:**

## 蟒蛇 3

```
# Python code to demonstrate the
# use of numpy.cov
import numpy as np

x = [1.23, 2.12, 3.34, 4.5]

y = [2.56, 2.89, 3.76, 3.95]

# find out covariance with respect  rows
cov_mat = np.stack((x, y), axis = 1)

print("shape of matrix x and y:", np.shape(cov_mat))

print("shape of covariance matrix:", np.shape(np.cov(cov_mat)))

print(np.cov(cov_mat))
```

**Output:** 

```
shape of matrix x and y: (4, 2)
shape of covariance matrix: (4, 4)
[[ 0.88445  0.51205  0.2793  -0.36575]
 [ 0.51205  0.29645  0.1617  -0.21175]
 [ 0.2793   0.1617   0.0882  -0.1155 ]
 [-0.36575 -0.21175 -0.1155   0.15125]]
```