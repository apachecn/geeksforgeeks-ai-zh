# Python 中的 SymPy |多面体. pgroup()

> 原文:[https://www . geesforgeks . org/sympy-多面体-pgroup-in-python/](https://www.geeksforgeeks.org/sympy-polyhedron-pgroup-in-python/)

**多面体. pgroup() : pgroup()** 是一个 sympy Python 库函数，返回多面体的排列。

> **语法:**组合学.多面体.多面体. pgroup()
> 
> **返回:**多面体的排列。

**代码#1 : pgroup()示例–四面体**

```
# Python code explaining
# SymPy.Polyhedron.pgroup()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.pgroup()

# Creating Polyhedron
a = tetrahedron.copy()

print ("Polyhedron - pgroup form : ", a.pgroup)

a.rotate(0)
print ("\nPolyhedron - pgroup form : ", a.pgroup)
```

**输出:**

> 多面体–组形式:置换组([
> (1 2 3)、
> (3)(0 1 2)、
> (0 3 2)、
> (0 3 1)、
> (0 1)(2 3)、
> (0 2)(1 3)、
> (0 3)(1 2)]
> 
> 多面体–组形式:置换组([
> (1 2 3)、
> (3)(0 1 2)、
> (0 3 2)、
> (0 3 1)、
> (0 1)(2 3)、
> (0 2)(1 3)、
> (0 3)(1 2)]

**代码#2 : pgroup()示例–八面体**

```
# Python code explaining
# SymPy.Polyhedron.pgroup()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.pgroup()

# Creating Polyhedron
a = octahedron.copy()

print ("Polyhedron - pgroup form : ", a.pgroup)

a.rotate(0)
print ("\nPolyhedron - pgroup form : ", a.pgroup)
```

**输出:**

> 多面体–组形式:置换组([
> (5)(1 2 3 4)、
> (0 4 5 2)、
> (0 1 5 3)、
> (0 1)(2 4)(3 5)、
> (0 2)(1 3)(4 5)、
> (0 3)(1 5)(2 4)、
> (0 4)(1 3)(2 5)、
> (0 5)(1 4)(2 3)、
> (0 5)(1 2)(3 4)、
> (0
> 
> 多面体–组形式:置换组([
> (5)(1 2 3 4)、
> (0 4 5 2)、
> (0 1 5 3)、
> (0 1)(2 4)(3 5)、
> (0 2)(1 3)(4 5)、
> (0 3)(1 5)(2 4)、
> (0 4)(1 3)(2 5)、
> (0 5)(1 4)(2 3)、
> (0 5)(1 2)(3 4)、
> (0