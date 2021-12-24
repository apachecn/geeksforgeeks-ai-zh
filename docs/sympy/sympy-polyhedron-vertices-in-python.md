# Python 中的 SymPy |多面体.顶点()

> 原文:[https://www . geesforgeks . org/sympy-多面体-python 中的顶点/](https://www.geeksforgeeks.org/sympy-polyhedron-vertices-in-python/)

**多面体.顶点() :顶点()**是一个返回多面体顶点的 sympy Python 库函数。

> **语法:**组合学.多面体.多面体.顶点()
> 
> **返回:**多面体的顶点。

**代码#1:顶点()示例–四面体**

```py
# Python code explaining
# SymPy.Polyhedron.vertices()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.vertices()

# Creating Polyhedron
a = tetrahedron.copy()

print ("Polyhedron - vertices form : ", a.vertices)

a.rotate(0)
print ("\nPolyhedron - vertices form : ", a.vertices)
```

**输出:**

> 多面体–顶点形式:(0，1，2，3)
> 
> 多面体–顶点形式:(0，2，3，1)

**代码#2:顶点()示例–八面体**

```py
# Python code explaining
# SymPy.Polyhedron.vertices()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.vertices()

# Creating Polyhedron
a = octahedron.copy()

print ("Polyhedron - vertices form : ", a.vertices)

a.rotate(0)
print ("\nPolyhedron - vertices form : ", a.vertices)
```

**输出:**

> 多面体–顶点形式:(0，1，2，3，4，5)
> 
> 多面体–顶点形式:(0，2，3，4，1，5)