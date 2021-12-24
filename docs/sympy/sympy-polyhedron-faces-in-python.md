# Python 中的 SymPy |多面体. faces()

> 原文:[https://www . geesforgeks . org/sympy-多面体-python 中的面/](https://www.geeksforgeeks.org/sympy-polyhedron-faces-in-python/)

**多面体. faces() : faces()** 是一个 sympy Python 库函数，返回多面体的面。

> **语法:**组合学.多面体.多面体.面()
> 
> **返回:**多面体的面。

**代码#1:面()示例–四面体**

```py
# Python code explaining
# SymPy.Polyhedron.faces()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.faces()

# Creating Polyhedron
a = tetrahedron.copy()

print ("Polyhedron - faces form : ", a.faces)

a.rotate(0)
print ("\nPolyhedron - faces form : ", a.faces)
```

**输出:**

> 多面体–面的形式:{(0，1，2)，(0，1，3)，(0，2，3)，(1，2，3)}
> 
> 多面体–面的形式:{(0，1，2)，(0，1，3)，(0，2，3)，(1，2，3)}

**代码#2:面()示例–八面体**

```py
# Python code explaining
# SymPy.Polyhedron.faces()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.faces()

# Creating Polyhedron
a = octahedron.copy()

print ("Polyhedron - faces form : ", a.faces)

a.rotate(0)
print ("\nPolyhedron - faces form : ", a.faces)
```

**输出:**

> 多面体–面的形式:{(0，1，2)，(0，1，4)，(0，2，3)，(0，3，4)，(1，2，5)，(1，4，5)，(2，3，5)，(3，4，5)}
> 
> 多面体–面的形式:{(0，1，2)，(0，1，4)，(0，2，3)，(0，3，4)，(1，2，5)，(1，4，5)，(2，3，5)，(3，4，5)}