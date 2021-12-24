# Python 中的 SymPy |多面体. edges()

> 原文:[https://www . geesforgeks . org/sympy-多面体-python 中的边/](https://www.geeksforgeeks.org/sympy-polyhedron-edges-in-python/)

**多面体. edges() : edges()** 是一个返回多面体边缘的 sympy Python 库函数。

> **语法:**
> 组合学.多面体.多面体.边()
> 
> **返回:**
> 多面体的边。

**代码#1:边()示例–四面体**

```
# Python code explaining
# SymPy.Polyhedron.edges()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.edges()

# Creating Polyhedron
a = tetrahedron.copy()

print ("Polyhedron - edges form : ", a.edges)

a.rotate(0)
print ("\nPolyhedron - edges form : ", a.edges)
```

**输出:**

> 多面体–边的形式:{(0，1)，(0，2)，(0，3)，(1，2)，(1，3)，(2，3)}
> 
> 多面体–边的形式:{(0，1)，(0，2)，(0，3)，(1，2)，(1，3)，(2，3)}

**代码#2:边()示例–八面体**

```
# Python code explaining
# SymPy.Polyhedron.edges()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.edges()

# Creating Polyhedron
a = octahedron.copy()

print ("Polyhedron - edges form : ", a.edges)

a.rotate(0)
print ("\nPolyhedron - edges form : ", a.edges)
```

**输出:**

> 多面体–边的形式:{(0，1)，(0，2)，(0，3)，…，(3，4)，(3，5)，(4，5)}
> 
> 多面体–边的形式:{(0，1)，(0，2)，(0，3)，…，(3，4)，(3，5)，(4，5)}