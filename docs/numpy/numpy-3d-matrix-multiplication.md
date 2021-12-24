# num py–3d 矩阵乘法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/num py-3d 矩阵乘法/

一个三维矩阵只不过是许多 2D 矩阵的集合(或堆叠)，就像 2D 矩阵是许多 1D 向量的集合/堆叠一样。因此，3D 矩阵的矩阵乘法涉及 2D 矩阵的多次乘法，最终归结为它们的行/列向量之间的点积。

让我们考虑形状(3，3，2)的矩阵 A 与形状(3，2，4)的另一个 3D 矩阵 B 相乘的例子。

## 巨蟒

```
import numpy as np

np.random.seed(42)

A = np.random.randint(0, 10, size=(3, 3, 2))
B = np.random.randint(0, 10, size=(3, 2, 4))

print("A:\n{}, shape={}\nB:\n{}, shape={}".format(
  A, A.shape, B, B.shape))
```