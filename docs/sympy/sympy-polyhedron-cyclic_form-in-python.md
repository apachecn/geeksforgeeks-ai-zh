# Python 中的 SymPy |多面体. cyclic_form()

> 原文:[https://www . geesforgeks . org/sympy-多面体-cyclic_form-in-python/](https://www.geeksforgeeks.org/sympy-polyhedron-cyclic_form-in-python/)

**多面体. cyclic_form() : cyclic_form()** 是一个 sympy Python 库函数，返回循环记数法中的角的索引。

> **语法:**
> 符号组合学.多面体.多面体.循环形式()
> 
> **返回:**
> 循环符号中的角索引

**代码#1:循环形式()示例–四面体**

```py
# Python code explaining
# SymPy.Polyhedron.cyclic_form()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.cyclic_form()

# Creating Polyhedron
a = tetrahedron.copy()

print ("Polyhedron - cyclic_form form : ", a.cyclic_form)

a.rotate(0)
print ("\nPolyhedron - cyclic_form form : ", a.cyclic_form)
```

**输出:**

> 多面体–循环形式形式:[]
> 
> 多面体–循环形式形式:[[1，2，3]]

**代码#2:循环形式()示例–八面体**

```py
# Python code explaining
# SymPy.Polyhedron.cyclic_form()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.cyclic_form()

# Creating Polyhedron
a = octahedron.copy()

print ("Polyhedron - cyclic_form form : ", a.cyclic_form)

a.rotate(0)
print ("\nPolyhedron - cyclic_form form : ", a.cyclic_form)
```

**输出:**

> 多面体–循环形式形式:[]
> 
> 多面体–循环形式形式:[[1，2，3，4]]