# Python 中的 SymPy |多面体. reset()

> 原文:[https://www . geesforgeks . org/sympy-多面体-python 中的重置/](https://www.geeksforgeeks.org/sympy-polyhedron-reset-in-python/)

**多面体. reset() : reset()** 是一个 sympy Python 库函数，它将角点返回到多面体的原始位置。

> **语法:**sympy . combinations .多面体.多面体. reset()
> 
> **返回:**角到多面体的原始位置

**代码#1:复位()示例–四面体**

```py
# Python code explaining
# SymPy.Polyhedron.reset()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.reset()

# Creating Polyhedron
a = tetrahedron.copy()

print ("Polyhedron - reset form : ", a.reset)

a.rotate(0)
print ("\nPolyhedron - reset form : ", a.reset)
```

**输出:**

> 多面体–重置形式:
> 
> 多面体–重置形式:

**代码#2:复位()示例–八面体**

```py
# Python code explaining
# SymPy.Polyhedron.reset()

# importing SymPy libraries
from sympy.combinatorics import Permutation, Cycle
from sympy.combinatorics.polyhedron import tetrahedron, octahedron

# Using from 
# sympy.combinatorics.polyhedron.Polyhedron.reset()

# Creating Polyhedron
a = octahedron.copy()

print ("Polyhedron - reset form : ", a.reset)

a.rotate(0)
print ("\nPolyhedron - reset form : ", a.reset)
```

**输出:**

> 多面体–重置形式:
> 
> 多面体–重置形式: