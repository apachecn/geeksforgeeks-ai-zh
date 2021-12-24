# Python 中的 SymPy |多面体. corners()

> 原文:[https://www . geesforgeks . org/sympy-多面体-python 中的角/](https://www.geeksforgeeks.org/sympy-polyhedron-corners-in-python/)

 **多面体. corners() : corners()** 是一个返回多面体角的 sympy Python 库函数。

> **语法:**
> 组合学.多面体.多面体.角()
> 
> **返回:**
> 多面体的角

**代码#1:拐角()示例–四面体**

```py
# Python code explaining
# SymPy.Polyhedron.corners()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.corners()

# Creating Polyhedron
a = tetrahedron.copy()

print ("Polyhedron - corners form : ", a.corners)

a.rotate(0)
print ("\nPolyhedron - corners form : ", a.corners)
```

**输出:**

> 多面体–角的形式:(0，1，2，3)
> 
> 多面体–角形:(0，2，3，1)

**代码#2:拐角()示例–八面体**

```py
# Python code explaining
# SymPy.Polyhedron.corners()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.corners()

# Creating Polyhedron
a = octahedron.copy()

print ("Polyhedron - corners form : ", a.corners)

a.rotate(0)
print ("\nPolyhedron - corners form : ", a.corners)
```

**输出:**

> 多面体–角的形式:(0，1，2，3，4，5)
> 
> 多面体–角的形状:(0，2，3，4，1，5)