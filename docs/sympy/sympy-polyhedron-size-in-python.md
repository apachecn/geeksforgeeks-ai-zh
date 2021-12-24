# Python 中的 SymPy |多面体. size()

> 原文:[https://www . geesforgeks . org/sympy-多面体-python 中的大小/](https://www.geeksforgeeks.org/sympy-polyhedron-size-in-python/)

**多面体. size() : size()** 是一个 sympy Python 库函数，返回多面体的角个数的计数。

> **语法:**sympy . combinations .多面体.多面体. size()
> 
> **返回:**计算多面体的角数

**代码#1:大小()示例–四面体**

```py
# Python code explaining
# SymPy.Polyhedron.size()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.size()

# Creating Polyhedron
a = tetrahedron.copy()

print ("Polyhedron - size form : ", a.size)

a.rotate(0)
print ("\nPolyhedron - size form : ", a.size)
```

**输出:**

> 多面体-尺寸形式:4
> 
> 多面体-尺寸形式:4

**代码#2:大小()示例–八面体**

```py
# Python code explaining
# SymPy.Polyhedron.size()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.size()

# Creating Polyhedron
a = octahedron.copy()

print ("Polyhedron - size form : ", a.size)

a.rotate(0)
print ("\nPolyhedron - size form : ", a.size)
```

**输出:**

> 多面体-尺寸形式:6
> 
> 多面体-尺寸形式:6