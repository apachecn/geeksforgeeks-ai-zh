# Python sympy | matrix . nullspace()方法

> 原文:[https://www . geesforgeks . org/python-sympy-matrix-nullspace-method/](https://www.geeksforgeeks.org/python-sympy-matrix-nullspace-method/)

借助**症状。矩阵()。零空间()**方法，我们可以找到一个矩阵的[零空间。**矩阵()。nullspace()** 返回跨越矩阵的 nullspace 的列向量列表。](https://www.cliffsnotes.com/study-guides/algebra/linear-algebra/real-euclidean-vector-spaces/the-nullspace-of-a-matrix)

> **语法:**矩阵()。nullspace()
> 
> **返回:**返回跨越矩阵零空间的列向量列表。

**示例#1:**

```py
# import sympy 
from sympy import * 

M = Matrix([[1, 0, 1, 3], [2, 3, 4, 7], [-1, -3, -3, -4]])
print("Matrix : {} ".format(M))

# Use sympy.nullspace() method 
M_nullspace = M.nullspace()  

print("Nullspace of a matrix : {}".format(M_nullspace))  
```

**输出:**

```py
Matrix : Matrix([[1, 0, 1, 3], [2, 3, 4, 7], [-1, -3, -3, -4]]) 
Nullspace of a matrix : [Matrix([
[  -1],
[-2/3],
[   1],
[   0]]), Matrix([
[  -3],
[-1/3],
[   0],
[   1]])]

```

**例 2:**

```py
# import sympy 
from sympy import * 

M = Matrix([[14, 0, 11, 3], [22, 23, 4, 7], [-12, -34, -3, -4]])
print("Matrix : {} ".format(M))

# Use sympy.nullspace() method 
M_nullspace = M.nullspace()  

print("Nullspace of a matrix : {}".format(M_nullspace)) 
```

**输出:**

```py
Matrix : Matrix([[14, 0, 11, 3], [22, 23, 4, 7], [-12, -34, -3, -4]]) 
Nullspace of a matrix : [Matrix([
[-1405/4254],
[   -10/709],
[  314/2127],
[         1]])]

```