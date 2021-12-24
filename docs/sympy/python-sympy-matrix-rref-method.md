# Python 症状| Matrix.rref()方法

> 原文:[https://www . geesforgeks . org/python-sympy-matrix-rref-method/](https://www.geeksforgeeks.org/python-sympy-matrix-rref-method/)

借助**症状。矩阵()。rref()** 法，我们可以把一个矩阵变成精简的[排梯队形式](https://en.wikipedia.org/wiki/Row_echelon_form)。**矩阵()。rref()** 返回两个元素的元组。第一种是简化的行梯队形式，第二种是透视列的索引元组。

> **语法:**矩阵()。rref()
> 
> **返回:**返回一个元组，其中第一个元素的类型为**矩阵**，第二个元素的类型为**元组**。

**示例#1:**

```py
# import sympy 
from sympy import * 

M = Matrix([[1, 0, 1, 3], [2, 3, 4, 7], [-1, -3, -3, -4]])
print("Matrix : {} ".format(M))

# Use sympy.rref() method 
M_rref = M.rref()  

print("The Row echelon form of matrix M and the pivot columns : {}".format(M_rref))  
```

**输出:**

```py
Matrix : Matrix([[1, 0, 1, 3], [2, 3, 4, 7], [-1, -3, -3, -4]]) 
The Row echelon form of matrix M and the pivot columns : (Matrix([
[1, 0,   1,   3],
[0, 1, 2/3, 1/3],
[0, 0,   0,   0]]), (0, 1))

```

**例 2:**

```py
# import sympy 
from sympy import * 

M = Matrix([[14, 0, 11, 3], [22, 23, 4, 7], [-12, -34, -3, -4]])
print("Matrix : {} ".format(M))

# Use sympy.rref() method 
M_rref = M.rref()  

print("The Row echelon form of matrix M and the pivot columns : {}".format(M_rref))  
```

**输出:**

```py
Matrix : Matrix([[14, 0, 11, 3], [22, 23, 4, 7], [-12, -34, -3, -4]]) 
The Row echelon form of matrix M and the pivot columns : (Matrix([
[1, 0, 0, 1405/4254],
[0, 1, 0,    10/709],
[0, 0, 1, -314/2127]]), (0, 1, 2))

```