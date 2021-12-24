# Python sympy | matrix . column space()方法

> 原文:[https://www . geesforgeks . org/python-sympy-matrix-column space-method/](https://www.geeksforgeeks.org/python-sympy-matrix-columnspace-method/)

借助**症状。矩阵()。columnspace()** 方法，我们可以找到一个矩阵的 [Columnspace。**矩阵()。columnspace()** 返回跨越矩阵列空间的列向量列表。](https://en.wikipedia.org/wiki/Row_and_column_spaces)

> **语法:**矩阵()。columnspace()
> 
> **返回:**返回跨越矩阵列空间的列向量列表。

**示例#1:**

```py
# import sympy 
from sympy import * 

M = Matrix([[1, 0, 1, 3], [2, 3, 4, 7], [-1, -3, -3, -4]])
print("Matrix : {} ".format(M))

# Use sympy.columnspace() method 
M_columnspace = M.columnspace()  

print("Columnspace of a matrix : {}".format(M_columnspace))  
```

**输出:**

```py
Matrix : Matrix([[1, 0, 1, 3], [2, 3, 4, 7], [-1, -3, -3, -4]]) 
Columnspace of a matrix : [Matrix([
[ 1],
[ 2],
[-1]]), Matrix([
[ 0],
[ 3],
[-3]])]

```

**例 2:**

```py
# import sympy 
from sympy import * 

M = Matrix([[14, 0, 11, 3], [22, 23, 4, 7], [-12, -34, -3, -4]])
print("Matrix : {} ".format(M))

# Use sympy.columnspace() method 
M_columnspace = M.columnspace()  

print("Columnspace of a matrix : {}".format(M_columnspace)) 
```

**输出:**

```py
Matrix : Matrix([[14, 0, 11, 3], [22, 23, 4, 7], [-12, -34, -3, -4]]) 
Columnspace of a matrix : [Matrix([
[ 14],
[ 22],
[-12]]), Matrix([
[  0],
[ 23],
[-34]]), Matrix([
[11],
[ 4],
[-3]])]

```