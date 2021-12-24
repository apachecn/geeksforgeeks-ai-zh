# Python 中的 SymPy |多面体. rotate()

> 原文:[https://www . geesforgeks . org/sympy-多面体-python 中的旋转/](https://www.geeksforgeeks.org/sympy-polyhedron-rotate-in-python/)

**多面体. rotate() : rotate()** 是一个关于多面体轴旋转的 sympy Python 库函数。

> **语法:**组合学.多面体.多面体.旋转()
> 
> **返回:**围绕多面体轴的旋转

**代码#1:旋转()示例–四面体**

```
# Python code explaining
# SymPy.Polyhedron.rotate()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.rotate()

# Creating Polyhedron
a = tetrahedron.copy()

print ("Polyhedron - rotate form : ", a.array_form)

# Rotating the axis
a.rotate(0)

print ("\nPolyhedron - rotate form : ", a.array_form)
```

**输出:**

> 多面体–旋转形状:[0，1，2，3]
> 
> 多面体–旋转形状:[0，2，3，1]

**代码#2:旋转()示例–八面体**

```
# Python code explaining
# SymPy.Polyhedron.rotate()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.rotate()

# Creating Polyhedron
a = octahedron.copy()

print ("Polyhedron - rotate form : ", a.array_form)

# Rotating the axis
a.rotate(0)

print ("\nPolyhedron - rotate form : ", a.array_form)
```

**输出:**

> 多面体–旋转形状:[0，1，2，3，4，5]
> 
> 多面体–旋转形状:[0，2，3，4，1，5]