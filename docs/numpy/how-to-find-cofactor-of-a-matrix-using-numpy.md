# 如何使用 Numpy

找到矩阵的辅因子

> 原文:[https://www . geeksforgeeks . org/如何使用-numpy/](https://www.geeksforgeeks.org/how-to-find-cofactor-of-a-matrix-using-numpy/) 找到矩阵的辅助因子

在本文中，我们将看到如何使用 NumPy 找到给定矩阵的辅助因子。没有直接的方法可以用 Numpy 找到给定矩阵的余因子。

### 利用 Numpy 中的矩阵求逆推导出求余因子的公式

**求矩阵逆的公式:**

```py
A-1 = ( 1 / det(A) )* Adj(A)      ----(1)
```

**Adj(A)是 A 的伴随矩阵，取 A 的辅因子矩阵的转置:**

```py
Adj(A) = (cofactor(A))T            ----(2)
```

**将等式 2 代入等式 1，我们得到如下结果:**

```py
A-1 = ( 1/det(A) ) *  (cofactor(A))T 
```

**将 det(A)发送到等式的另一侧:**

```py
det(A) * A-1 = (cofactor(A))T 
```

移除等式右侧的转置将导致在等式左侧(LHS)应用转置。我们可以在将 A <sup>-1</sup> 乘以 det(A)之后应用转置，但是为了简单起见，我们将转置应用到 A <sup>-1</sup> 然后乘以 det(A)，然而，两个结果是相同的。

```py
det(A) * (A-1)T = cofactor(A)      
```

**最后**、**我们推导出求矩阵辅因子的公式:**

```py
cofactor(A) = (A-1)T * det(A)
```

### Numpy 中的实现:

**所需步骤:**

*   求给定矩阵的[行列式](https://www.geeksforgeeks.org/how-to-calculate-the-determinant-of-a-matrix-using-numpy/)。
*   找到 [的](https://www.geeksforgeeks.org/how-to-inverse-a-matrix-using-numpy/)[逆矩阵](https://www.geeksforgeeks.org/how-to-inverse-a-matrix-using-numpy/)并将其转置。

**例 1:在 2D 矩阵中寻找辅因子**

## 蟒蛇 3

```py
import numpy as np

def matrix_cofactor(matrix):

    try:
        determinant = np.linalg.det(matrix)
        if(determinant!=0):
            cofactor = None
            cofactor = np.linalg.inv(matrix).T * determinant
            # return cofactor matrix of the given matrix
            return cofactor
        else:
            raise Exception("singular matrix")
    except Exception as e:
        print("could not find cofactor matrix due to",e)

print(matrix_cofactor([[1, 2], [3, 4]]))
```

**输出:**

```py
[[ 4\. -3.]
 [-2\.  1.]]
```

**例 2:求辅因子 3D 矩阵**

## 蟒蛇 3

```py
import numpy as np

def matrix_cofactor(matrix):

    try:
        determinant = np.linalg.det(matrix)
        if(determinant!=0):
            cofactor = None
            cofactor = np.linalg.inv(matrix).T * determinant
            # return cofactor matrix of the given matrix
            return cofactor
        else:
            raise Exception("singular matrix")
    except Exception as e:
        print("could not find cofactor matrix due to",e)

print(matrix_cofactor([[1, 9, 3],
                       [2, 5, 4],
                       [3, 7, 8]]))
```

**输出:**

```py
[[ 12\.  -4\.  -1.]
 [-51\.  -1\.  20.]
 [ 21\.   2\. -13.]]
```